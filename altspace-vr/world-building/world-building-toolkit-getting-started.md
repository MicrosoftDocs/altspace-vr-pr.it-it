---
title: Introduzione a Altspace Uploader
description: Informazioni su come configurare e caricare i mondi AltspaceVR usando i modelli di scena unity con Altspace Uploader.
ms.date: 09/29/2021
ms.author: v-vtieto
ms.topic: article
keywords: toolkit, Altspace, uploader
ms.openlocfilehash: 8d71551fe552159c0078105307802774f44c0d47
ms.sourcegitcommit: 8c58f9f9ad1a3f9534141dee2c78e32792d0db7a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2021
ms.locfileid: "130298811"
---
# <a name="introducing-the-altspace-uploader"></a>Introduzione a Altspace Uploader

> [!NOTE]
> - Se si è interessati, iscriversi al [disco ufficiale altspaceVR](https://discordapp.com/invite/altspacevr) e visitare il canale #world-building.  
> - Se si sta tentando di rigenerare uno spazio precedente, vedere la [guida all'aggiornamento](upgrading-old-unity-projects.md). 

Uploader consente di usare una scena unity come modello per i mondi. È possibile ospitare una casa infestata per Halloween o la creazione preferita da Minecraft. Se è possibile importarlo in Unity, è possibile ottenerlo in Altspace in questo modo. Ecco alcuni esempi [di Worlds](https://account.altvr.com/worlds/1046572460192825569).

![Mondi di esempio](images/unity-uploader-img-01.png)

## <a name="setup"></a>Eseguire la configurazione

1. Partecipare al disco ufficiale [altspaceVR](https://discordapp.com/invite/altspacevr) e visitare il canale #world-building. Gli amici non consentono agli amici di creare worlds da soli.
2. Per informazioni [di base, Attività iniziali](world-building-getting-started.md) guida alla creazione del mondo
3. [Installare Unity Hub](https://unity3d.com/get-unity/download) e **Unity 2020.3.9.** Il caricatore non funzionerà a meno che non si corrisponda esattamente a questa versione. Se non si ha un account Unity gratuito, è necessario. Durante l'installazione, scegliere la versione **Personale** (perché si sta eseguendo questa operazione per divertimento) e assicurarsi di eseguire le operazioni seguenti:
    * Includere il **modulo Supporto compilazione Android.**
    * Nella Windows, includere il **modulo Mac Build Support (Mono).**
    * In Mac includere il modulo **Windows build support (Mono).**
4. [Scaricare AltspaceVR Uploader](https://aka.ms/AvrUrpUploader)
5. [Creare un modello nel](https://account.altvr.com/space_templates/new) sito Web. Assegnare **Hello World modello**.
6. [Creare un world](https://account.altvr.com/worlds/my) e assegnare **il nome Hello World**. Selezionare **Hello World modello** come modello.

![Schermata del mondo creato](images/unity-uploader-img-02.png)

## <a name="upload-your-scene"></a>Upload la scena

> [!NOTE]
> Una guida dettagliata è disponibile [qui.](https://buildingthemetaverse.medium.com/how-to-make-your-own-altspace-templates-and-kits-unity-2020-3-9-uploader-2-x-5b40e92bb759)

1. Aprire Unity Hub e creare un nuovo progetto Unity 2020.3.9. Per il modello selezionare **Universal Render Pipeline**.

    ![Scegliere il modello URP Unity](images/001-unity-templates.png)

1. Passare alla cartella in cui è stato scaricato Altspace Uploader e quindi copiarla o spostarla da tale cartella alla cartella radice del nuovo progetto Unity.
1. In Unity sulla barra dei menu selezionare **Finestra**  >  **Gestione pacchetti.**
1. Nella barra Gestione pacchetti menu selezionare l'elenco a discesa segno più ("+" ) e quindi selezionare **Aggiungi pacchetto da tarball**.
1. Passare alla cartella che contiene Altspace Uploader, selezionare il caricatore e quindi fare clic su **Apri**.  Dopo il caricamento del pacchetto, **altspaceVR** viene visualizzato sulla barra dei menu:

    ![ALTSPACEVR sulla barra dei menu](images/002-altspacevr-on-menu-bar.png)

> [!NOTE]
> È necessario importare il pacchetto Altspace Uploader in ogni progetto Unity che si vuole usare con Altspace.
1. Sulla barra dei menu selezionare **AltspaceVR > Modelli**.
1. Nella finestra di dialogo Altspace VR Templates (Modelli **VR altspace)** accedere con le credenziali dell'account Altspace. (l'account di accesso msa sarà disponibile a breve. Se è stato eseguito solo l'accesso ad Altspace con il account Microsoft, è necessario creare una password usando l'opzione "Password dimenticata" nel sito Web.
1. Fare clic **sull'elenco a** discesa Selezionare un modello e quindi **selezionare Hello World modello**.
1. Scegliere una scena: fare clic sul pulsante Con i puntini di sospensione (tre puntini) per scegliere un file con estensione **unity,** passare alla cartella **Assets** Scenes nel progetto e quindi selezionare  >   **SampleScene.unity** e aprirla.
1. In **Build for platforms (Compila** per piattaforme): assicurarsi che Windows selezionata.  Per il momento, le altre due opzioni, **Android** **e Mac,** **non devono** essere selezionate. Una volta che si vuole che gli utenti visitino, è consigliabile compilare e caricare per tutte le piattaforme."
1. Selezionare il **pulsante & Upload** compilazione. Questo processo può richiedere uno o due minuti.
1. Avviare Altspace, selezionare **Menu principale** e quindi nella barra dei menu selezionare **My Worlds**.
1. Passare a **Hello World** e quindi aprirlo.

    La scena dovrebbe essere simile a quella vista nell'editor di Unity.

## <a name="whats-supported"></a>Attività supportate

* Sì: modelli, collisioni, animazioni, effetti delle particelle, audio, skybox e così via.
* No: script. Per motivi di sicurezza, i caricamenti contenenti script verranno rifiutati.
* Forse: cose fantasiose come l'illuminazione globale dinamica.
* Upload scene per piattaforme diverse separatamente o insieme.
* Vedere [Mondo in primo piano](https://account.altvr.com/worlds/featured). Molte sono state compilate usando lo strumento di caricamento.

## <a name="tips"></a>Suggerimenti

* Partecipare alla [discordia altspaceVR ufficiale.](https://discordapp.com/invite/altspacevr)
* Nella pagina Modello sul lato sinistro vengono visualizzati i caricamenti più recenti in base alla piattaforma. Se l'operazione ha avuto esito positivo, vengono visualizzati **1-2 minuti fa.** 

![Pannello Modelli aperto con i caricamenti evidenziati](images/template-upload-list.png)

* È possibile essere nel mondo quando si esegue l'aggiornamento. Nel momento in cui il **caricatore Upload completa,** è possibile reimpostare il mondo per visualizzare le modifiche.
* Quando si compila solo per PC con una scena semplice, è necessario meno di un minuto per visualizzare una modifica in Altspace.
* Impostare World su Private e Unlisted per evitare distrazioni.
* Posizionare un cubo all'origine in modo da visualizzare la posizione in cui verranno generati gli utenti per impostazione predefinita. Nascondere il cubo durante il caricamento.

## <a name="troubleshooting"></a>Risoluzione dei problemi

**Sto cadendo o non riesco a teletrasportarmi su nulla** È necessario aggiungere la collisione agli oggetti per teletrasportarli.

**Non è cambiato nulla**
    * La scena è stata salvato in Unity?
    * È stata scelta la piattaforma su cui si sta testando?
    * Sei nel mondo giusto? È stato scelto il modello giusto nel modulo Uploader AND in the World?
    * Sono stati controllate le statistiche della pagina Modello?

**Upload ha esito negativo o si verifica il timeout**
    * L'errore di caricamento più comune si verifica quando la versione di Unity non è corretta. È necessario corrispondere esattamente alla versione richiesta.
    * Il caricamento potrebbe essere troppo grande. Provare a mantenere le scene del PC < 100 MB. Iniziare con piccole dimensioni e sviluppare. Ottimizzare, ottimizzare, ottimizzare.
    * Provare con un nuovo progetto che contiene un cubo semplice.
    * Non forzare l'uscita durante una compilazione. Può danneggiare la scena. Provare a ricaricare il file.

**Si tratta di un processo lento**
    * È consigliabile compilare solo per PC durante l'iterazione e per Android in un secondo momento.
    * Provare a rimuovere i file inutilizzati. Per qualsiasi motivo, Unity talvolta diventa troppo zealoso.

**Non è possibile accedere con le credenziali altspace**
    * Per i messaggi di posta elettronica viene fatto distinzione tra maiuscole e minuscole.
    * Provare con un nuovo progetto.
    * Assicurarsi che l'account Altspace sia in regola.

## <a name="see-also"></a>Vedi anche

* [Unity Learn](https://unity3d.com/learn)
* [Forum di Unity](https://forum.unity.com)  
