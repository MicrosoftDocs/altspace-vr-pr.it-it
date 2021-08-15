---
title: Importazione di modelli glTF
description: Informazioni su come importare correttamente modelli glTF 3D nelle esperienze altspaceVR e risolvere eventuali problemi.
ms.date: 03/11/2021
ms.topic: article
keywords: modelli, glTF, importazione, sketchfab, risoluzione dei problemi
ms.openlocfilehash: 527c38fc49028258fa432445fe14a355710a18be65ee74252a8c39bc1bfe5190
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119127061"
---
# <a name="importing-gltf-models"></a>Importazione di modelli glTF

> [!NOTE]
> Questa funzionalità è attualmente disponibile per utenti selezionati nel programma di accesso anticipato.

Un modo per portare i modelli e le scene 3D in Altspace è usare lo [standard glTF.](https://en.wikipedia.org/wiki/GlTF) È possibile caricare un file con estensione glb (glTF in pacchetto) per creare un modello che è possibile generare in un secondo momento nell'editor del mondo. Si tratta di un'alternativa [al caricamento di kit personalizzati.](uploading-custom-kits.md) È consigliabile creare modelli per dimostrazioni rapide perché non è necessario usare Unity e kit per ottimizzare le prestazioni e la riusabilità. 

1. Trovare alcuni asset glTF 3D. Una posizione in cui eseguire la ricerca è Sketchfab (provare a filtrare **i modelli scaricabili** come [questo).](https://sketchfab.com/search?features=downloadable&q=low+poly+wolf&sort_by=-pertinence&type=models) Una volta trovato, selezionare **Download 3D Model (Scarica modello 3D):**

![Modello di cane 3D da Sketchfab](images/importing-models-img-01.png)

2. Copiare il collegamento al modello e leggere i requisiti di licenza. 
3. Scaricare la **versione glTF (Autoconverted Format)**

![Opzioni di download di Sketchfab con il formato convertito automaticamente evidenziato](images/importing-models-img-02.png)

4. Aprire il [sito GLB Packer](https://glb-packer.glitch.me) e selezionare la casella **Convert PNG to JPEG (beta) (Converti PNG in JPEG - beta)**
5. Decomprimere i file glTF scaricati e trascinarli tutti contemporaneamente nella scheda del browser GLB Packer

![Finestra che mostra la decompressione del modello](images/importing-models-img-03.png)

6. A seconda del numero e delle dimensioni dei file, l'elaborazione potrebbe richiedere del tempo. Al termine dell'elaborazione, verrà scaricato un file **out.glb.** Rinominare il file con un nome informativo, che sarà il nome dell'oggetto nel mondo(ad esempio **Low Poly Wolf.glb)**
7. Passare a [Altvr.com > altri > e](https://account.altvr.com/users/sign_in) selezionare **Crea**
8. Specificare il percorso del file con estensione glb e assicurarsi di copiare il collegamento Sketchfab nella descrizione per l'attribuzione. Se si vuole, è possibile specificare un'immagine di anteprima, quindi **selezionare Crea modello:**

![Anteprima del modello in AltspaceVR](images/importing-models-img-04.png)

9. Selezionare **Copia negli Appunti**
10. Aprire World **Editor > Altspace > Basics > GLTF**
11. Incollare l'URL e selezionare **Conferma**

Congratulazioni. È stato appena generato il primo modello.

## <a name="troubleshooting"></a>Risoluzione dei problemi

**Quando si fa clic su **Conferma non è** successo nulla**
    * Attualmente è previsto un limite di 100.000 poligoni. Se l'operazione non riesce, eliminare l'oggetto per evitare potenziali problemi con gli utenti che si uniscono al mondo
    * Potrebbero verificarsi altri problemi con l'asset. Provare a usare gli asset con il numero di poligoni più possibile.
    * Il modello che si sta portando può essere di piccole o grandi dimensioni. Provare ad aumentare/ridurre la scala o a spostare l'avatar. È possibile che ci si trova all'interno del modello.

**Caricamento lento** La velocità con cui altri utenti nel mondo lo caricano dipenderà dalla velocità di connessione. Non viene inoltre memorizzato nella cache come asset kit. Se ne viene posizionata una nella home page, si finisce per scaricare di nuovo lo stesso modello ogni volta che si partecipa, il che non è eccezionale.

**Non si verifica alcuna collisione** Per impostazione predefinita, non si verifica alcuna collisione sugli oggetti che vengono portati in questo modo

**Quando viene generato, i controlli** vengono persi in sei file DOF o sono all'interno, quindi è difficile modificarlo Sì, questi problemi sono noti e ci auguriamo di poterli risolvere a breve.  