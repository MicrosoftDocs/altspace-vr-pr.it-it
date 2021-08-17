---
title: Caricamento di kit personalizzati
description: Informazioni su come configurare, generare e caricare kit personalizzati in AltspaceVR, oltre alla Guida alla risoluzione dei problemi.
ms.date: 03/11/2021
ms.topic: article
keywords: kit, caricamento, risoluzione dei problemi
ms.openlocfilehash: 9a90bff2360d854dc398a35501f07cddcbce5c6c66ef8230f2e412a022f8aed0
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119125527"
---
# <a name="uploading-custom-kits"></a>Caricamento di kit personalizzati

World Editor include kit contenenti Artifacts che è possibile generare nel mondo. Ad esempio, [Il Kit Campifire ha](https://account.altvr.com/kits/993516233267609824) molti tipi di alberi: ogni tipo di albero è un artefatto. Per creare un kit personalizzato, è necessario creare AssetBundles di Unity e caricare un file .zip contenente un prefab Unity per ogni artefatto e registrare ogni artefatto nel sito Web. Fortunatamente, unity Uploader basato sulla community automatizza la maggior parte del flusso di lavoro. Dopo il caricamento, è possibile generare oggetti dai propri kit nei propri worlds e altri utenti possono vederli automaticamente. In un secondo momento, è possibile condividere il kit con gli amici o anche con l'intero Community in primo piano.

## <a name="prerequisites"></a>Prerequisiti

1. [Installare Unity Hub e Unity](world-building-toolkit-getting-started.md)
2. Scaricare la versione più recente di [Unity Uploader](https://altvr.com/download-latest-unity-uploader/)

## <a name="setup"></a>Eseguire la configurazione 

> [!VIDEO https://channel9.msdn.com/Shows/Docs-Mixed-Reality/How-to-upload-my-own-Kits-Part-1-Setup/player]

1. Creare un kit nel sito Web [in Worlds > Kits](https://account.altvr.com/kits)
2. Copiare l'ID kit dalla barra degli indirizzi del browser negli Appunti (questo passaggio sarà più semplice in Uploader versioni 0.9+)
3. Creare un nuovo Project Unity
4. Importare lo caricatore Unity facendo doppio clic sul pacchetto

![Pacchetto del caricatore Unity importato](images/custom-kits-img-01.png)

5. Accedere a Uploader con l'indirizzo di posta elettronica e la password di Altspace

![Interfaccia di accesso altspaceVR in Unity](images/custom-kits-img-02.png)

## <a name="generate-and-upload-your-kit"></a>Generare e caricare il kit

> [!VIDEO https://channel9.msdn.com/Shows/Docs-Mixed-Reality/How-to-upload-my-own-Kits-Part-2/player]

1. Compilare **Kit Folder Name** (Nome cartella kit) con l'ID kit come prefisso e un tema (ad **esempio, 1137484494681408069_pirates)** e compilare Kit Asset Name (Nome **asset kit)** con l'ID kit come prefisso. Tutti gli asset dovranno avere questo prefisso.

![Interfaccia altspaceVR in Unity con il nome della cartella kit](images/custom-kits-img-03.png)

2. Per ogni artefatto o set di Artifacts:
* Trascinare i prefab di origine nella scheda Gerarchia
* Selezionare quelli da includere in un set, ad esempio cinque tipi di punti
* Aggiornare il nome **dell'asset kit** con **il nome**
* Selezionare **Convert GameObject(s) to Kit Prefab (Converti GameObject in prefab kit)**
* Verificare che siano stati creati nuovi prefab e screenshot nella cartella Assets/Prefabs

![Interfaccia altspaceVR in Unity con elementi selezionati](images/custom-kits-img-04.png)

> [!NOTE]
> Per apportare modifiche a un prefab generato, trascinarlo di nuovo nella gerarchia, apportare modifiche e quindi fare clic su Applica nella scheda Controllo per aggiornare il prefab.  

3. Quando si è pronti, scorrere verso il basso la scheda Uploader (Caricatore) e preparare la generazione di un file ZIP con il bundle di asset
4. Per un'iterazione più veloce, **deselezionare build kit per Android?**. Ricordarsi di compilare e caricare una versione per Android in un secondo momento al termine dell'operazione di iterazione o di condivisione/funzionalità del kit. 
5. Selezionare **Load Kit Prefab Directories (Directory prefab di Load Kit)**
6. Scegliere **Build** (Compila) accanto a quello corrispondente al nome della cartella kit. È comune produrre più kit dallo stesso progetto Unity. Questa operazione può richiedere del tempo a seconda delle dimensioni del kit. Al termine, la cartella contenente il file ZIP verrà aperta automaticamente. 
7. Passare al sito Web, modificare il kit creato in precedenza e caricare il file ZIP prodotto. Questo caricamento può richiedere del tempo a seconda delle dimensioni del file.
    * Se l'operazione ha esito positivo, sul lato sinistro vengono visualizzati in "Carica" le dimensioni dei file e per PC e Android e la data dell'ultimo aggiornamento
    * Se l'operazione ha esito negativo, assicurarsi che non siano presenti script, che non siano supportati. Questi script vengono cercati per la sicurezza e riprovare.

Congratulazioni! È ora possibile creare Worlds con il proprio kit.

## <a name="troubleshooting"></a>Risoluzione dei problemi 

**Sono previsti limiti?**
Non esistono ancora limiti rigidi, ma tenere presente che gli utenti devono scaricare AssetBundle per la propria piattaforma per l'intero kit anche se viene usato un solo artefatto. Provare a mantenere il download per piattaforma a 5 MB o meno. Un modo per eseguire questa operazione è suddividere gli elementi in kit più piccoli. Ad esempio, 200 proprietà devono essere suddivise a metà. 

**Si vede "split eye"?**
Reimportare l'ultima versione di Uploader per ottenere le impostazioni di rendering più recenti

**Aggiornamenti/modifiche non riflesse?**
    * Controllare l'ora aggiornata nella pagina Kit
    * L'accesso a World non funzionerà: riavviare il client. Anche in questo modo l'aggiornamento potrebbe richiedere alcuni minuti
    * Assicurarsi che non siano presenti spazi nei nomi delle cartelle o nei nomi di prefab, ad esempio **"party_favors" e "party favors"**

**Continua a dire che ho uno script, ma non lo so** A volte Il browser AssetBundle include automaticamente i file. Provare a isolare il modello che si sta portando. Ad esempio, non trascinarlo quando fa già parte di un altro prefab

**E per quanto riguarda i sistemi di particelle e le animazioni?**
Per queste operazioni, è necessario posizionarle in un cubo 1x1x1 posizionato in corrispondenza dell'origine con Rendering mesh e Collisione disabilitati. I sistemi di particelle devono avere il ciclo abilitato e **il ridimensionamento** deve essere impostato su **Gerarchia** in modo da poterli ridimensionare correttamente in Altspace. Dopo aver generato i prefab per tutte le animazioni, disabilitare le collisioni sugli oggetti **collisione** per ognuno.

**I Artifacts sono scuri** Il material shader del modello è stato impostato su **Mobile/Vertex lit-only directional lights**?

**L'artefatto non è rivolto nel modo giusto** Ruotare **il modello** e il **collisore** e aggiornare il prefab. La rotazione dell'elemento padre non consente di eseguire alcun'operazione, che viene ignorata. È possibile usare il campo **Sostituzione rotazione** per eseguire facilmente questa operazione.

**Questi Artifacts possono essere usati con la funzione **CreateFromLibrary** dell'SDK?**
Sì