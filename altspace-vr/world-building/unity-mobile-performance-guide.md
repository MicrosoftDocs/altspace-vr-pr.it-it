---
title: Guida alle prestazioni di AltspaceVR Mobile
description: Informazioni su come usare varie proprietà di Unity per rendere i mondi performanti su dispositivi mobili come Oculus Quest
ms.date: 04/20/2021
ms.topic: article
keywords: world editor, performance, oculus, quest, unity, textures, lightmaps, stats, profiler, draw calls, altspacevr, uploader
ms.openlocfilehash: d5689e245c10ccb61abdd0aaa2327132d4374bb7e53a2eaec316d991b38378fb
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126979"
---
# <a name="altspacevr-mobile-performance-guide"></a>Guida alle prestazioni di AltspaceVR Mobile

## <a name="main-points"></a>**Punti principali:**

* **72 FPS** in Oculus Quest 1 e 2, è la destinazione.
* **La riduzione delle chiamate di disegno** tramite l'invio in batch statico è essenziale e mira **a meno di 25 chiamate**
* **Un materiale per oggetto per** favorire l'invio in batch statico (suddividere gli oggetti multi-materiale in oggetti separati).
* **Nella** maggior parte dei casi, gli oggetti in un ambiente devono essere impostati su **"Static".**
* **Una mappa** di luce per scena, una 2k o una 4k per l'intera scena, ~25 texel per unità, il ridimensionamento della mappa di luce deve essere ottimizzato per ogni oggetto (grafico di ridimensionamento seguente)
* **Usare** shader di qualità mobile (ad esempio, "Mobile/Diffuse" e così via), evitare lo shader/PBR/Reflection Probes/Light Probes di Unity Standard perché si tratta di operazioni pesanti e nel caso dei probe verranno aggiunti chiamate di disegno.
* **Meno di 100.000 triangoli** sullo schermo
* **Occlusion Culling** consente di ridurre i poligoni su schermo, anche se è previsto un costo iniziale per l'attivazione dell'occlusione, quindi misurare l'effetto sulla frequenza dei fotogrammi in Altspace usando il pannello di diagnostica.
* Per tutte **le trame** in una scena, usare **'Override for Android'** e impostarle su **RGB(A) Compressed ASTC 6x6 block format**.  Lasciare la compressione predefinita Impostazioni build Android (disponibile in: File/Build Impostazioni/Android/Texture Compression: 'Don't override'), in modo che Lightmaps non otterrà la compressione ASTC.  In questo modo e condividendo i materiali tra gli oggetti, si prova a mantenere il pacchetto unity della scena a circa **10-20 MB per Android.**

L'obiettivo generale è raggiungere un framerate accettabile tra i dispositivi: in Oculus Quest 1 e 2 idealmente la scena verrà eseguita a 72 FPS da tutti i punti di vista quando la scena viene popolata, anche se un intervallo di 60-72 FPS è spesso un obiettivo più realistico.

Framerate può essere misurato all'interno di AltspaceVR in qualsiasi dispositivo in uso (disponibile nell'app AltspaceVR in **Impostazioni/Support/Show Diagnostics Panel/FPS).**

Un rundown degli strumenti unity standard disponibili per ottimizzare meglio le scene:

## <a name="stats-panelframe-debuggerprofiler"></a>**Pannello statistiche/Debugger frame/Profiler**

* Questi strumenti saranno i migliori amici per migliorare le prestazioni della scena.  È possibile farvi riferimento solo mentre la scena è In esecuzione **nell'editor,** perché i relativi valori saranno diversi da quando la scena non è in riproduzione, ovvero l'invio in batch statico automatico non verrà eseguito quando la scena non è in riproduzione.

* **Il pannello Statistiche** (visualizzabile nella visualizzazione del gioco in 'Statistiche') mostra la quantità di **batch/batch salvati, chiamate SetPass e framerate.**

    * Batch: quantità di chiamate di disegno correnti visibili dal punto di vista della fotocamera corrente.  **Meno di 25 batch per** un ambiente è un buon obiettivo da raggiungere.
    * Batch salvati (visibili solo quando la scena è **In riproduzione):** quantità di chiamate di disegno ridotte tramite batch statico o creazione di istanze GPU
    * Chiamate SetPass: numero di materiali visibili diversi in una scena
    * Framerate: la quantità di fotogrammi al secondo nella visualizzazione Gioco (offre un'idea approssimativa di ciò che accade; le scene devono sempre essere testate in-app, in-headset, usando il pannello Oculus Framerate perché la lettura fps sarà sempre diversa da quella nell'editor)

* **Debugger frame** (disponibile in Window/Analysis/Frame Debugger).  Il pannello statistiche in , se abilitato, consente di visualizzare ciò che la GPU sta disegnando per creare l'immagine finale, visualizzando un elenco di drawcall dal primo all'ultimo.  Verranno spiegati i motivi per cui una chiamata di disegno non è stata in batch con una chiamata di disegno precedente ,ovvero "Questo oggetto usa un materiale diverso" o "Questo oggetto usa una mappa di luce diversa", ed è un ottimo modo per sviluppare una comprensione di ciò che accade nella scena e di come e perché determinate scelte visive possono essere costose dal punto di vista del calcolo.

* **Profiler** mostrerà le parti del computer in uso in qualsiasi momento durante l'esecuzione del gioco. Utile per determinare dove si verifica il collo di bottiglia delle prestazioni.  Ad esempio, se si verifica un utilizzo elevato della CPU nella scena, è possibile che siano presenti troppe chiamate di disegno o che si verifichi un utilizzo elevato della GPU, potrebbe verificarsi un eccessivo ridisegno ,ovvero il numero di volte in cui viene eseguito il rendering di un singolo pixel per produrre l'immagine finale, che può essere causato dalla presenza di più superfici trasparenti,  o oggetti che non vengono espulsi quando non sono visualizzabili.

## <a name="draw-calls-shadersmaterialsobjects"></a>**Chiamate di disegno (shader/materiali/oggetti)**

* Ogni volta che è necessario eseguire il rendering di uno shader, un materiale o un oggetto, la CPU deve indicare alla GPU dell'opzione (nota anche come "chiamate di disegno", colloquialmente **"drawcalls").**  Ovvero, se si hanno 5 shader, 10 materiali e 20 oggetti, con qualsiasi valore maggiore; si hanno circa 20 drawcall.  Altri elementi che possono moltiplicare le drawcall includono la presenza di oggetti in mappe di luce diverse o la presenza di più di una luce in tempo reale in una scena ,ovvero una luce punto aggiungerà un'altra chiamata a ogni oggetto che si trova all'interno del relativo intervallo, quindi in genere è consigliabile evitare qualsiasi elemento diverso dalla luce direzionale di una scena.  I probe di reflection e i probe di luce moltiplicheranno anche le chiamate di disegno su qualsiasi oggetto raggiunto, quindi devono essere evitati.

*  L'invio in batch statico di oggetti che condividono materiali simili in un singolo oggetto quando vengono inviati alla GPU (con Occlusion Culling che elimina le mesh non visualizzate), quindi impostando tutti gli oggetti nell'esempio precedente su "Static", si riduce la scena a circa 10 drawcall, 1 per ogni materiale. 

* **I batch di** materiali si verificano quando un oggetto ha i materiali esatti come un altro oggetto, ma se un oggetto ha più materiali, non esegue il batch con un oggetto con meno materiali.  Per questo motivo: gli oggetti DEVONO avere solo **1 materiale** e gli oggetti che usano più materiali devono essere suddivisi in oggetti separati per ogni materiale.  **I batch di** materiali possono essere ridotti tramite **Texture Atlasing** (combinando trame di più oggetti univoci per condividere un singolo foglio di trama in modo che usino tutti lo stesso materiale).  Se possibile, provare a mantenere la quantità di Atlas fino a una singola trama/materiale da 2.000 o 4000 per scena.

## <a name="scene-complexity"></a>**Complessità della scena**

* **Geometria:** provare a mantenere i triangoli sullo schermo per ambienti inferiori a 100.000.  Usare la scheda "Statistiche" nel pannello Gioco di Unity per vedere il triangolo che si sta toccando da vari punti di osservazione nella scena.  Le proprietà di questo tipo devono essere nell'intervallo "centinaia" di triangoli, con solo oggetti di proprietà "hero" importanti nell'intervallo di migliaia di triangoli. 

* È tecnicamente possibile usare i **LOD** (mesh a livello di dettaglio), anche se la soluzione lightmap predefinita di Unity non condivide i dati della mappa della luce tra i LOD, quindi è possibile ottenere artefatti lightmapping quando i LOD passano a questa risoluzione.  In alternativa, è possibile usare il componente gruppo lod per il culling della distanza semplice, anche se l'oggetto non ha mesh loD inferiori:

![Finestra Gruppo LOD in Unity](images/world-building-lod-Group.png)

* **Occlusion Culling** riduce il numero di oggetti di cui viene eseguito il rendering solo a ciò che si trova all'interno del frustum di visualizzazione della fotocamera e che sono immediatamente visibili (ovvero gli oggetti che sono Occluded dalla visualizzazione sono Culled).  L'culling di occlusione deve essere quasi sempre cotto per la scena e i livelli devono essere progettati per supportarla, ovvero se si dispone di un livello elevato, è possibile usare le pareti o gli oggetti di grandi dimensioni per suddividere la linea di visualizzazione del giocatore, in modo che non possano sempre vedere fino all'estremità opposta del livello.  Le impostazioni predefinite del bake dovrebbero funzionare, anche se potrebbe essere necessario ridurre i valori "Occluder più piccolo" o "Più piccolo foro".  Per oggetti come recinti in cui è possibile vedere le crepe nell'oggetto o gli oggetti trasparenti, è consigliabile disattivare lo stato "Occluder" dell'oggetto nel menu a discesa "Statico" in modo che gli oggetti dietro di esso non siano erroneamente oclusi. 

## <a name="lightmaps"></a>**Mappe di luce**

* Idealmente solo **una mappa di luce per scena** (una 2k o una 4k per tutto), in caso di errore; meno mappe di luce con risoluzioni più elevate sono migliori rispetto a molte mappe di luce con risoluzioni inferiori.
* La presenza di più mappe di luce può influire anche sul numero di chiamate di disegno, in quanto gli oggetti che hanno o non dispongono di mappe di luce saranno in batch diversi e altre mappe di luce saranno anche in batch diversi.
* In genere, dovrebbe essere sufficiente una risoluzione lightmap di **circa 25 texel per** unità (impostare la risoluzione nelle impostazioni illuminazione/scena).  Se si dispone di spazio aggiuntivo nella mappa delle luci, è possibile aumentare questo valore.
* Modificare **l'impostazione Lightmap Scaling** per oggetto in modo che la risoluzione sia salvata per gli oggetti che ne hanno bisogno. 

* **Grafico di scalabilità della** mappa di luce (regola generale) 
    * **Primo** piano (livello geografico attraversabile): 1 
    * **Props** (in particolare props più piccoli di un essere umano): **2-3** (per evitare artefatti lightmap e seams sugli oggetti) 
    * **Area intermedia** (geometria appena esterna all'area attraversabile e/o oggetti di grandi dimensioni come gli edifici): **0,5**
    * **Sfondo** (vista/oggetti distanti): **0,02** 
    * **Transparent Surfaces** (come glass): **0** (con 'Cast/Receive Shadows' disabilitato) 

Inoltre, come baseline, ecco alcune impostazioni usate per l'ambiente effetto Screen Door:

![Finestra di illuminazione in Unity](images/world-building-lightmaps.png)

Nota: se si usano queste impostazioni, è possibile impostare Lightmapper su "GPU Lightmapper" e impostare Lightmap Size su "2048" per bakes di anteprima molto più veloci e quindi eseguire il backup su CPU e 4k per il bake finale.

## <a name="texture-compressionfile-size"></a>**Compressione trama/Dimensioni file**

* Per la build Android, si prova a mantenere le dimensioni della scena del pacchetto Unity fino a circa 10-20 MB totali.  A tale scopo, si condividono materiali generici tra molti oggetti, usando il colore dei vertici per colorare gli oggetti e impostando sostituzioni manuali per Android in modo che le trame usino la compressione a blocchi **ASTC 6x6,** che sarà inferiore alla compressione predefinita.

* Il motivo per cui non si impostano le impostazioni di compilazione android per l'uso di ASTC è che le mappe di luce non hanno un aspetto positivo con tale compressione (molti artefatti in blocchi), ed è necessario impostare la mappa di luce per usare ETC dopo ogni bake, quindi è più semplice configurare l'override per tutte le trame della scena una sola volta che aggiornare le impostazioni di compressione della mappa di luce dopo ogni bake.

![Finestra trama in Unity](images/world-building-texutres.png)

* Inoltre, l'impostazione delle trame per l'uso della modalità filtro trilineare con un livello anisotropo di 2 può aiutarle a rimanere affilate agli angoli di visualizzazione.

Altri suggerimenti e consigli sulle prestazioni sono disponibili nella documentazione relativa al miglioramento [delle prestazioni del mondo](improving-performance.md).
