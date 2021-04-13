---
title: Importazione di modelli glTF
description: Informazioni su come importare correttamente i modelli glTF 3D nelle esperienze di AltspaceVR e risolvere eventuali problemi.
ms.date: 03/11/2021
ms.topic: article
keywords: modelli, glTF, importazione, Sketchfab, risoluzione dei problemi
ms.openlocfilehash: 4489f90832bd1cf85ff161caed11684257cce6ab
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213260"
---
# <a name="importing-gltf-models"></a>Importazione di modelli glTF

> [!NOTE]
> Questa funzionalità è disponibile per gli utenti selezionati nel programma di accesso anticipato al momento.

Un modo per portare i modelli e le scene 3D in Altspace consiste nell'usare lo [standard glTF](https://en.wikipedia.org/wiki/GlTF). È possibile caricare un file con estensione GLB (compresso glTF) per creare un modello che è possibile generare in un secondo momento nell'editor mondiale. Si tratta di un'alternativa al [caricamento di kit personalizzati](uploading-custom-kits.md). È consigliabile creare modelli per dimostrazioni rapide perché non è necessario usare Unity e kit quando si desidera ottimizzare le prestazioni e la riusabilità. 

1. Trovare alcune risorse glTF 3D. Una posizione in cui eseguire la ricerca è Sketchfab (provare a filtrare per modelli **scaricabili** come [questo](https://sketchfab.com/search?features=downloadable&q=low+poly+wolf&sort_by=-pertinence&type=models)). Una volta individuato, selezionare **Scarica modello 3D**:

![modello Dog 3D da Sketchfab](images/importing-models-img-01.png)

2. Copiare il collegamento al modello e leggere i requisiti di licenza. 
3. Scaricare la versione **glTF (autoconverted Format)**

![Opzioni di download di Sketchfab con formato convertito automaticamente evidenziato](images/importing-models-img-02.png)

4. Aprire il sito di [GLB Packer](https://glb-packer.glitch.me) e selezionare la casella **Converti png in JPEG (beta)**
5. Decomprimere i file glTF scaricati e trascinarli tutti contemporaneamente nella scheda del browser GLB Packer

![Finestra che mostra la decompressione del modello](images/importing-models-img-03.png)

6. A seconda del numero e delle dimensioni dei file, l'elaborazione potrebbe richiedere del tempo. Al termine dell'elaborazione, verrà scaricato un file **out. glb** . Rinominare il file con informazioni informative: si tratta del nome dell'oggetto in tutto il mondo, ad esempio **Low Poly Wolf. glb**
7. Passare a [altvr.com > altri modelli di >](https://account.altvr.com/users/sign_in) e selezionare **Crea**
8. Specificare il percorso del file con estensione GLB e assicurarsi di copiare il collegamento Sketchfab nella descrizione per l'attribuzione. Se lo si desidera, è possibile specificare un'immagine di anteprima, quindi selezionare **Crea modello**:

![Anteprima modello in AltspaceVR](images/importing-models-img-04.png)

9. Selezionare **copia negli Appunti**
10. Aprire l' **Editor del mondo > Altspace > nozioni di base > GLTF**
11. Incollare l'URL e selezionare **conferma**

Congratulazioni. È stato appena generato il primo modello.

## <a name="troubleshooting"></a>Risoluzione dei problemi

**Quando si fa clic su **conferma** non è successo nulla**
    * È attualmente disponibile un limite di 100.000 poligoni. In caso di errore, eliminare l'oggetto per evitare potenziali problemi relativi agli utenti che si uniscono al mondo
    * Potrebbero esserci altri problemi con l'asset. Provare a usare asset con il minor numero di poligoni possibile.
    * Il modello che si sta inserendo può essere piccolo o grande. Provare ad aumentare o ridurre la scala o spostare l'avatar in un modello.

**Il caricamento è lento** La velocità di caricamento da parte di altri utenti in tutto il mondo dipenderà dalla velocità di connessione. Inoltre, non viene memorizzato nella cache come asset Kit. Se ne viene inserito uno nella Home page, si esaurirà il download dello stesso modello ogni volta che si partecipa, che non è eccezionale.

Non **ci sono collisioni** Per impostazione predefinita, non esiste alcuna collisione sugli oggetti portati in questo modo

**Quando viene generato, perdo i miei controlli su sei DOF o sono all'interno di, quindi è difficile modificarlo** Sì, sono consapevoli di questi problemi e ci auguriamo di risolverli a breve.  