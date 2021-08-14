---
title: Guida alle prestazioni di AltspaceVR Mobile
description: Informazioni su come usare varie proprietà di Unity per rendere il mondo più performante nei dispositivi mobili come Oculus Quest
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

* **72 FPS** in Oculus Quest 1 e 2, è l'obiettivo.
* **La riduzione delle chiamate di disegno tramite l'invio** in batch statico è essenziale e mira **a meno di 25 chiamate di disegno**
* **Un materiale per oggetto per** favorire l'invio in batch statico (suddividere gli oggetti multi-materiale in oggetti separati).
* **Nella** maggior parte dei casi, gli oggetti in un ambiente devono essere impostati su **"Static".**
* Una mappa di luce **per scena,** una 2k o una 4k per l'intera scena, ~25 texel per unità, il ridimensionamento della mappa della luce deve essere ottimizzato per ogni oggetto (grafico di ridimensionamento riportato di seguito)
* **Usare** shader di qualità mobile (ad esempio, "Mobile/Diffuse" e così via), evitare shader/PBR/Probe di reflection/Probe di reflection Unity standard perché si tratta di operazioni pesanti e nel caso dei probe verranno aggiunti chiamate di disegno.
* **Meno di 100.000 triangoli** sullo schermo
* Il **Culling dell'occlusione** consente di ridurre i poligoni su schermo, anche se è previsto un costo iniziale per l'a attivazione del culling dell'occlusione, quindi misurare l'effetto sulla frequenza dei fotogrammi in Altspace usando il pannello di diagnostica.
* Per tutte **le trame** in una scena, usare **"Override per Android"** e impostarle su **RGB(A) Compressed ASTC 6x6 block format (Formato blocco ASTC 6x6 compresso).**  Lasciare l'impostazione predefinita per la compressione Impostazioni build Android (disponibile in: File/Build Impostazioni/Android/Texture Compression: 'Don't override'), in modo che lightmaps non otterrà la compressione ASTC.  Eseguendo questa operazione e condividendo materiali tra gli oggetti, si prova a mantenere il pacchetto Unity della scena a circa **10-20 MB per Android.**

L'obiettivo generale è raggiungere una frequenza dei fotogrammi accettabile tra i dispositivi: in Oculus Quest 1 e 2 idealmente la scena verrà eseguita a 72 FPS da tutti i punti di vista quando la scena viene popolata, anche se un intervallo di 60-72 FPS è spesso un obiettivo più realistico.

La frequenza dei fotogrammi può essere misurata all'interno di AltspaceVR in qualsiasi dispositivo in uso (disponibile nell'app AltspaceVR in **Impostazioni/Support/Show Diagnostics Panel/FPS**).

Un rundown degli strumenti Unity standard disponibili per ottimizzare meglio le scene:

## <a name="stats-panelframe-debuggerprofiler"></a>**Pannello Statistiche/Debugger frame/Profiler**

* Questi strumenti saranno i migliori amici per migliorare le prestazioni della scena.  È possibile farvi riferimento solo mentre la scena è In riproduzione **nell'editor, perché** i relativi valori saranno diversi da quando la scena non viene riprodotta(ovvero, l'invio in batch statico automatico non verrà eseguito quando la scena non è in riproduzione)

* **Il pannello Statistiche** (visualizzabile nella visualizzazione del gioco in 'Statistiche') mostrerà la quantità di **batch/batch salvati, le chiamate SetPass e la frequenza dei frame.**

    * Batch: quantità di chiamate di disegno correnti visibili dal punto di vista della fotocamera corrente.  **Meno di 25 batch per** un ambiente sono un buon obiettivo.
    * Batch salvati (visibile solo quando la scena è **In riproduzione):** quantità di chiamate di disegno ridotte tramite batch statici o istanze GPU
    * Chiamate SetPass: numero di materiali visibili diversi in una scena
    * Frequenza dei fotogrammi: la quantità di fotogrammi al secondo nella visualizzazione del gioco (offre un'idea approssimativa di ciò che accade; le scene devono essere sempre testate in-app, nel visore VR, usando il pannello Oculus Framerate perché il readout fps sarà sempre diverso da quello nell'editor)

* **Debugger frame** (disponibile in Finestra/Analisi/Debugger frame).  Il pannello Delle statistiche, se abilitato, consentirà di vedere cosa disegna la GPU per creare l'immagine finale, visualizzando un elenco di drawcall dalla prima all'ultima.  Verranno spiegati i motivi per cui una chiamata di disegno non è stata in batch con una chiamata di disegno precedente ,ovvero "Questo oggetto usa un materiale diverso" o "Questo oggetto usa una mappa di luce diversa", ed è un ottimo modo per sviluppare una comprensione di ciò che accade nella scena e di come e perché determinate scelte visive possono essere costose dal punto di vista del calcolo.

* **Profiler** mostrerà quali parti del computer vengono usate in qualsiasi momento durante l'esecuzione del gioco. Utile per determinare dove le prestazioni causano colli di bottiglia.  Ad esempio, se si verifica un utilizzo elevato della CPU nella scena, è possibile che siano presenti troppe chiamate di disegno o che si verifichi un utilizzo elevato della GPU, potrebbe verificarsi un eccessivo disegno (ovvero il numero di volte in cui viene eseguito il rendering di un singolo pixel per produrre l'immagine finale), il che può essere causato dalla presenza di più superfici trasparenti,  Oggetti o non in corso di culled quando non sono visualizzabili.

## <a name="draw-calls-shadersmaterialsobjects"></a>**Chiamate di disegno (shader/materiali/oggetti)**

* Ogni volta che è necessario eseguire il rendering di uno shader, di un materiale o di un oggetto, la CPU deve indicare alla GPU del commutatore (nota anche come "draw call", ovvero **"drawcall").**  Ovvero, se si dispone di 5 shader, 10 materiali e 20 oggetti, a seconda del valore maggiore; Si hanno circa 20 drawcall.  Altri elementi che possono moltiplicare le drawcall includono la presenza di oggetti in mappe di luce diverse o la presenza di più di una luce in tempo reale in una scena (ovvero, una luce punto aggiungerà un'altra chiamata di disegno a ogni oggetto all'interno del relativo intervallo), quindi in genere è consigliabile evitare qualsiasi elemento diverso dalla luce direzionale di una scena.  Anche i probe di reflection e i probe leggeri moltiplicano le chiamate di disegno su qualsiasi oggetto che hanno raggiunto, quindi devono essere evitati.

*  L'invio in batch statico esegue il batch di oggetti che condividono materiali simili in un singolo oggetto quando vengono inviati alla GPU (con Occlusion Culling che elimina le mesh che non sono visualizzate), quindi impostando tutti gli oggetti nell'esempio precedente su 'Static', si riduce la scena a circa 10 drawcall, 1 per ogni materiale. 

* **I batch di** materiali si verificano quando un oggetto ha i materiali esatti come un altro oggetto, ma se un oggetto ha più materiali, non verrà eseguito il batch con un oggetto con meno materiali.  Per questo motivo: **gli oggetti DEVONO avere solo 1 materiale** e gli oggetti che usano più materiali devono essere suddivisi in oggetti separati per ogni materiale.  **I batch di materiali** possono essere ridotti tramite **Texture Atlasing** (che combina trame di più oggetti univoci per condividere un singolo foglio di trama in modo che usino tutti lo stesso materiale).  Se possibile, provare a mantenere la quantità di Atlases fino a una singola trama/materiale da 2k o 4k per scena.

## <a name="scene-complexity"></a>**Complessità della scena**

* **Geometria:** provare a mantenere i triangoli sullo schermo per ambienti inferiori a 100.000.  Usa la scheda 'Stats' (Statistiche) nel pannello Game (Gioco) di Unity per vedere quali triangoli vengono conteggiati dai vari punti di vista della scena.  Le proprietà come tali devono essere nell'intervallo "centinaia" di triangoli, con solo proprietà "hero" importanti nell'intervallo di migliaia di triangoli. 

* Tecnicamente è possibile usare i **LOD** (livello di mesh di dettaglio), anche se la soluzione lightmap predefinita di Unity non condivide i dati della mappa della luce tra i LOD, pertanto è possibile ottenere artefatti di mapping di luce quando i LOD passano a questa risoluzione.  In alternativa, è possibile usare il componente LOD Group per il semplice Culling delle distanze, anche se l'oggetto non ha mesh LOD inferiori:

![Finestra LoD Group (Gruppo di oggetti loD) in Unity](images/world-building-lod-Group.png)

* **Il Culling di occlusione** riduce il numero di oggetti di cui viene eseguito il rendering solo a ciò che si trova all'interno del frustum di visualizzazione della fotocamera e che sono immediatamente visibili (ovvero, gli oggetti che sono occlusi dalla visualizzazione sono Culled).  Il culling dell'occlusione dovrebbe essere quasi sempre in bake per la scena e i livelli devono essere progettati per supportarla, ovvero se si dispone di un livello elevato, è possibile usare le pareti o gli oggetti di grandi dimensioni per suddividere la linea di vista del giocatore, in modo che non possano sempre passare fino all'estremità opposta del livello.  Le impostazioni predefinite del bake dovrebbero funzionare, anche se potrebbe essere necessario ridurre i valori "Occluder più piccolo" o "Foro più piccolo".  Per oggetti come i recinti in cui è possibile vedere le crepe nell'oggetto o gli oggetti trasparenti, è necessario disattivare lo stato "Occluder" dell'oggetto nel menu a discesa "Statico" in modo che gli oggetti dietro di esso non siano erroneamente occlusi. 

## <a name="lightmaps"></a>**Mappe di luce**

* Idealmente, solo **una mappa di luce per scena** (una 2k o una 4k per tutto), in caso non lo sia; un numero inferiore di mappe di luce con risoluzioni più elevate è migliore di molte mappe di luce con risoluzioni inferiori.
* La presenza di più mappe di luce può influire anche sul numero di chiamate di disegno, in quanto gli oggetti che hanno o non hanno mappe di luce saranno in batch diversi e altre mappe di luce saranno anche in batch diversi.
* In genere, dovrebbe essere sufficiente una risoluzione lightmap di circa **25 texel per** unità (impostare la risoluzione nelle impostazioni Illuminazione/Scena).  Se si dispone di spazio aggiuntivo nella mappa della luce, è possibile aumentare questo valore.
* Modificare **l'impostazione Lightmap Scaling** per ogni oggetto in modo che la risoluzione sia salvata per gli oggetti che ne hanno bisogno. 

* **Grafico di scala della mappa della** luce (regola generale) 
    * **Primo piano** (livello geografico attraversabile): 1 
    * **Proprietà (in** particolare proprietà più piccole di un essere umano): **2-3** (per evitare artefatti e sgheghe della mappa della luce sugli oggetti) 
    * **Midground** (Geometria che si trova all'esterno dell'area attraversabile e/o di oggetti di grandi dimensioni come edifici): **0,5**
    * **Sfondo** (vista/oggetti distanti): **0,02** 
    * **Transparent Surfaces** (come glass): **0** (con 'Cast/Receive Shadows' disabilitato) 

Inoltre, come base di riferimento, ecco alcune impostazioni usate per l'ambiente effetto Screen Door:

![Finestra di illuminazione in Unity](images/world-building-lightmaps.png)

Nota: se si usano queste impostazioni, è possibile impostare Lightmapper su 'GPU Lightmapper' e impostare Lightmap Size su '2048' per bake di anteprima molto più veloci e quindi eseguire il backup su CPU e 4 KB per il bake finale.

## <a name="texture-compressionfile-size"></a>**Compressione trama/Dimensioni file**

* Per la build Android, si tenta di mantenere le dimensioni della scena del pacchetto Unity fino a circa 10-20 MB in totale.  A tale scopo, si condividono materiali generici tra molti oggetti, usando il colore dei vertici per tdeterminare gli oggetti e impostando sostituzioni manuali per Android in modo che le trame usino la compressione a blocchi **ASTC 6x6,** che sarà più piccola della compressione predefinita.

* Il motivo per cui non si impostano le impostazioni di compilazione di Android per l'uso di ASTC è che le mappe di luce non hanno un aspetto positivo con tale compressione (molti artefatti bloccanti) ed è necessario impostare la mappa della luce per l'uso di ETC dopo ogni bake, quindi è più semplice configurare l'override per tutte le trame della scena una sola volta che aggiornare le impostazioni di compressione della mappa della luce dopo ogni bake.

![Finestra trama in Unity](images/world-building-texutres.png)

* Inoltre, l'impostazione delle trame per l'uso della modalità filtro trilineare con un livello anisotropo 2 può essere utile per mantenere la nitidezza degli angoli di visualizzazione.

Altri suggerimenti e consigli sulle prestazioni sono disponibili nella documentazione [Improving world performance (Miglioramento delle prestazioni del mondo).](improving-performance.md)
