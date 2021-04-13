---
title: Caricamento di kit personalizzati
description: Informazioni su come configurare, generare e caricare i propri kit personalizzati in AltspaceVR, oltre alla guida alla risoluzione dei problemi.
ms.date: 03/11/2021
ms.topic: article
keywords: Kit, caricamento, risoluzione dei problemi
ms.openlocfilehash: e5a1b9c2ef5339db0cb821cb6f7d21a930416451
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213508"
---
# <a name="uploading-custom-kits"></a>Caricamento di kit personalizzati

Nell'editor mondiale sono disponibili kit contenenti artefatti che è possibile generare in tutto il mondo. Ad esempio, il [Kit falò](https://account.altvr.com/kits/993516233267609824) presenta molti tipi di alberi, ognuno dei quali è un artefatto. Per creare un kit personalizzato, è necessario creare Unity AssetBundles e caricare un file con estensione zip contenente una prefabbricata Unity per ogni artefatto e registrare ogni artefatto nel sito Web. Fortunatamente, il caricatore di Unity guidato dalla community automatizza la maggior parte del flusso di lavoro. Una volta caricato, è possibile generare oggetti dai propri kit nei propri mondi e altri utenti possono visualizzarli automaticamente. In seguito, è possibile condividere il kit con i propri amici o anche con l'intera community in primo piano.

## <a name="prerequisites"></a>Prerequisiti

1. [Installare Hub Unity e Unity](world-building-toolkit-getting-started.md)
2. Scaricare la versione più recente dell' [Uploader Unity](https://altvr.com/download-latest-unity-uploader/)

## <a name="setup"></a>Eseguire la configurazione 

> [!VIDEO https://channel9.msdn.com/Shows/Docs-Mixed-Reality/How-to-upload-my-own-Kits-Part-1-Setup/player]

1. Crea un kit nel nostro sito Web in [worlds > Kit](https://account.altvr.com/kits)
2. Copiare l'ID Kit dalla barra degli indirizzi del browser negli Appunti (questo passaggio sarà più semplice nelle versioni di Uploader 0.9 +)
3. Creare un nuovo progetto Unity
4. Importare l'Uploader Unity facendo doppio clic sul pacchetto

![Pacchetto di caricamento Unity importato](images/custom-kits-img-01.png)

5. Accedere al caricatore con la posta elettronica e la password di Altspace

![Interfaccia di accesso AltspaceVR in Unity](images/custom-kits-img-02.png)

## <a name="generate-and-upload-your-kit"></a>Generare e caricare il kit

> [!VIDEO https://channel9.msdn.com/Shows/Docs-Mixed-Reality/How-to-upload-my-own-Kits-Part-2/player]

1. Inserire il **nome della cartella kit** con l'ID Kit come prefisso e un tema (ad esempio, **1137484494681408069_pirates**) e inserire il **nome dell'asset** del kit con l'ID Kit come prefisso. Tutti gli asset dovranno avere questo prefisso.

![Interfaccia AltspaceVR in Unity con il nome della cartella kit](images/custom-kits-img-03.png)

2. Per ogni artefatto o set di elementi:
* Trascinare i prefabbricati di origine nella scheda gerarchia
* Selezionare quelli da includere in un set, ad esempio cinque tipi di barilotti
* Aggiornare il **nome dell'asset del kit** con **Barrel**
* Selezionare **Converti GameObject in kit prefabbricato**
* Verificare che nella cartella assets/prefabbricates siano stati creati nuovi prefabbricati e schermate

![Interfaccia AltspaceVR in Unity con gli elementi selezionati](images/custom-kits-img-04.png)

> [!NOTE]
> Se si desidera apportare modifiche a una prefabbricata generata, trascinarla di nuovo nella gerarchia, apportare modifiche e quindi fare clic su **applica** nella scheda controllo per aggiornare la prefabbricata. 

3. Quando si è pronti, scorrere la scheda Uploader e prepararsi a generare un file zip con il bundle di asset
4. Per un'iterazione più veloce, deselezionare il **Kit di compilazione per Android**. Ricordarsi di compilare e caricare una versione per Android in un secondo momento, al termine dell'iterazione o se si vuole condividere/includere il kit. 
5. Selezionare le **directory di Load Kit prefabbricate**
6. Scegliere **Compila** accanto a quello corrispondente al nome della cartella del kit. È comune produrre più kit dallo stesso progetto Unity. L'operazione potrebbe richiedere alcuni minuti, a seconda delle dimensioni del kit. Al termine, la cartella che contiene il file zip verrà aperta automaticamente. 
7. Accedere al sito Web, modificare il kit creato in precedenza e caricare il file zip prodotto. Questo caricamento potrebbe richiedere alcuni minuti a seconda delle dimensioni del file.
    * In caso di esito positivo, verrà visualizzato sul lato sinistro sotto "carica" le dimensioni dei file e per PC e Android e dopo l'ultimo aggiornamento
    * In caso di esito negativo, assicurarsi che non siano presenti script, non sono supportati gli script, vengono verificati per la sicurezza e riprovare.

Congratulazioni! Sei pronto per creare mondi con il tuo kit.

## <a name="troubleshooting"></a>Risoluzione dei problemi 

**Sono previsti limiti?**
Non esistono ancora limiti rigidi, ma tenere presente che gli utenti devono scaricare AssetBundle per la piattaforma per l'intero kit anche se viene usato un solo artefatto. Provare a lasciare il download per piattaforma a 5 MB o meno. Un modo per eseguire questa operazione consiste nel suddividere gli elementi in kit più piccoli. Ad esempio, 200 le prop devono essere suddivise a metà. 

**Visto "Split Eye"?**
Reimportare il caricatore più recente per ottenere le impostazioni di rendering corrette

**Aggiornamenti/modifiche non riflesse?**
    * Controllare l'ora aggiornata nella pagina del kit
    * Il riavvio del mondo non funzionerà. riavviare il client. Anche in questo modo potrebbero essere necessari alcuni minuti per l'aggiornamento
    * Assicurarsi che non siano presenti spazi nei nomi di cartella o nei nomi di prefabbricati **, ad esempio,' party_favors ' rispetto a' entità predilige '**

**Continua a dire che ho uno script ma non** Il browser AssetBundle include automaticamente file a volte. Provare a isolare il modello che si sta introducendo. Ad esempio, non trascinarlo quando fa parte di un altro prefabbricato

**Quali sono i sistemi particellari e le animazioni?**
Per questi elementi, successivamente in un cubo 1x1x1 posizionato all'origine con il rendering e la collisione della mesh disabilitati. Per i sistemi particellari è necessario abilitare il ciclo e il **ridimensionamento** deve essere impostato su **gerarchia** in modo che sia possibile ridimensionarli in Altspace correttamente. Dopo aver generato i prefabbricati per tutte le animazioni, disabilitare i conflitti sugli oggetti **collisione** per ciascuno di essi.

**Gli artefatti sono scuri** Il Material shader del modello è stato impostato su **luci direzionali solo per dispositivi mobili/Vertex illuminate**?

**L'artefatto non è rivolte al modo giusto** Ruotare il **modello** e il **Collider** e aggiornare la prefabbricata. La rotazione dell'elemento padre non esegue alcuna operazione, che viene ignorata. Per eseguire questa operazione in modo semplice, è possibile usare il campo di **sostituzione della rotazione** .

**È possibile usare questi artefatti con la funzione **CreateFromLibrary** dell'SDK?**
Sì