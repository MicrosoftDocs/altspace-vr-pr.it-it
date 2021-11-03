---
title: Introduzione a Altspace Uploader
description: Informazioni su come configurare e caricare gli scenari AltspaceVR usando i modelli di scena unity con Altspace Uploader.
ms.date: 10/29/2021
ms.author: v-vtieto
ms.topic: article
ms.openlocfilehash: 6d28b3efe75d589a0a09d4969add5d043a3116d0
ms.sourcegitcommit: 20605c50a93852f93a3464c5c339f6a7da67a047
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/03/2021
ms.locfileid: "131278963"
---
# <a name="introducing-the-altspace-uploader"></a>Introduzione a Altspace Uploader

> [!NOTE]
> - Se si è interessati, partecipare al [discord altspaceVR](https://discordapp.com/invite/altspacevr) ufficiale e visitare il canale #world-building.  
> - Se si sta provando a ritascire uno spazio precedente, vedere la [guida all'aggiornamento](upgrading-old-unity-projects.md). 

Uploader consente di usare una scena unity come modello per i propri scenari. È possibile ospitare una casa infestata per Il Mio o la creazione preferita da Minecraft. Se è possibile importarlo in Unity, è probabile che sia possibile ottenerlo in Altspace in questo modo. Ecco alcuni esempi [di Worlds](https://account.altvr.com/worlds/1046572460192825569).

![Mondo di esempio](images/unity-uploader-img-01.png)

## <a name="setup"></a>Eseguire la configurazione

1. Partecipa alla [discord di AltspaceVR ufficiale](https://discordapp.com/invite/altspacevr) e visita il #world-building. Gli amici non consentono agli amici di creare worlds da soli.
2. Per le [nozioni di base, Attività iniziali guida](world-building-getting-started.md) alla creazione del mondo
3. [Installare Unity Hub](https://blogs.unity3d.com/2018/01/24/streamline-your-workflow-introducing-unity-hub-beta) e [**installare 2020.3.18f1**](https://unity3d.com/unity/whats-new/2020.3.18). Uploader non funzionerà a meno che non si corrisponda esattamente a questa versione. Se non si ha un account Unity gratuito, è necessario scegliere **Personal** (Personale) perché si tratta di un'operazione divertente. Durante l'installazione, assicurarsi di selezionare **l'opzione Compilazioni Android** e disabilitare l'aggiornamento automatico.
    * Includere il **modulo Android Build Support (Supporto compilazione Android).**
    * In Windows, includere il **modulo Mac Build Support (Mono) (Supporto compilazione Mac - Mono).**
    * In Mac includere il modulo **Windows Build Support (Mono).**
4. [Scaricare la versione più recente di Unity Uploader](https://altvr.com/download-latest-unity-uploader)
5. [Creare un modello](https://account.altvr.com/space_templates/new) nel sito Web. Assegnare al **Hello World il nome Template**.
6. [Creare un oggetto World](https://account.altvr.com/worlds/my) e denotarlo **Hello World**. Selezionare **Hello World modello** come Modello.

![Schermata Del mondo creato](images/unity-uploader-img-02.png)

## <a name="upload-your-scene"></a>Upload la scena

> [!NOTE]
> Una guida dettagliata è disponibile [qui.](https://buildingthemetaverse.medium.com/how-to-make-your-own-altspace-templates-and-kits-unity-2020-3-9-uploader-2-x-5b40e92bb759)

1. Aprire Unity Hub e creare un nuovo progetto Unity 2020.3.9. Per il modello, selezionare **Universal Render Pipeline (Pipeline di rendering universale).**

    ![Scegliere il modello UrP Unity](images/001-unity-templates.png)

1. Passare alla cartella in cui è stato scaricato Altspace Uploader e quindi copiarlo o spostarlo da tale cartella alla cartella radice del nuovo progetto Unity.
1. Nella barra dei menu di Unity selezionare **Window**  >  **Gestione pacchetti (Finestra Gestione pacchetti).**
1. Nella barra Gestione pacchetti menu a discesa selezionare l'elenco a discesa con il segno più ("+") e quindi selezionare **Aggiungi pacchetto da tarball.**
1. Passare alla cartella che contiene altspace Uploader, selezionare l'uploader e quindi fare clic su **Apri.**  Dopo il caricamento del pacchetto, **altspaceVR** viene visualizzato sulla barra dei menu:

    ![ALTSPACEVR sulla barra dei menu](images/002-altspacevr-on-menu-bar.png)

> [!NOTE]
> È necessario importare il pacchetto di Altspace Uploader in ogni progetto Unity che si vuole usare con Altspace.
1. Sulla barra dei menu selezionare **ALTSPACEVR > Modelli**.
1. Nella finestra **di dialogo Altspace VR Templates (Modelli VR altspace)** accedere con le credenziali dell'account Altspace. L'account di accesso dell'account del servizio microsoft sarà presto disponibile. Se è stato eseguito l'accesso solo ad Altspace con il account Microsoft, è necessario creare una password usando l'opzione "Password dimenticata" nel sito Web.
1. Fare clic **sull'elenco a** discesa Selezionare un modello e quindi **selezionare Hello World modello**.
1. Scegliere una scena: fare clic sul pulsante con i puntini di sospensione Choose **a .unity file** (Scegli un file con estensione unity) (tre puntini), passare alla cartella **Assets** Scenes (Scene asset) nel progetto e quindi selezionare  >   **SampleScene.unity** e aprirla.
1. In **Build for platforms (Compila per** le piattaforme): assicurarsi **Windows** sia selezionata. Per il momento, le altre due opzioni, **Android** **e Mac,** **non devono** essere selezionate. Quando si vuole che gli utenti visitino, è consigliabile compilare e caricare per tutte le piattaforme."
1. Selezionare il **pulsante & Upload** compilazione. Questo processo può richiedere uno o due minuti.
1. Avviare ALTSPACE, selezionare **Menu principale** e quindi sulla barra dei menu selezionare **My Worlds.**
1. Passare a **Hello World** e quindi aprirlo.

    La scena dovrebbe essere simile a quella vista nell'editor di Unity.

## <a name="whats-supported"></a>Attività supportate

* Sì: modelli, collisioni, animazioni, effetti particella, audio, skybox e così via.
* No: script. Per motivi di sicurezza, i caricamenti contenenti script verranno rifiutati.
* Forse: qualcosa di speciale come l'illuminazione globale dinamica.
* Upload scene per piattaforme diverse separatamente o insieme.
* Vedere [Featured Worlds (Mondo in primo piano).](https://account.altvr.com/worlds/featured) Molte sono state compilate usando uploader.

## <a name="tips"></a>Suggerimenti

* Partecipare alla [discord di AltspaceVR ufficiale.](https://discordapp.com/invite/altspacevr)
* Nella pagina Modello sul lato sinistro vengono visualizzati i caricamenti più recenti in base alla piattaforma. Se l'operazione ha avuto esito positivo, **vengono visualizzati 1-2 minuti fa.** 

![Pannello Modelli aperto con i caricamenti evidenziati](images/template-upload-list.png)

* È possibile essere nel mondo quando si esegue l'aggiornamento. Nel momento in cui uploader **Upload completa,** è possibile reimpostare il mondo per visualizzare le modifiche.
* Quando si compila solo per PC con una scena semplice, la modifica in Altspace dovrebbe richiedere meno di un minuto.
* Imposta World su Private (Privato) e Unlisted (Non in elenco) per evitare distrazioni.
* Posizionare un cubo nell'origine in modo che sia possibile vedere dove verranno generati gli utenti per impostazione predefinita. Nascondere il cubo durante il caricamento.

## <a name="troubleshooting"></a>Risoluzione dei problemi

**I'm falling or can't teleport onto anything** È necessario aggiungere collisioni agli oggetti per teletrasportarli.

**Non sono state modificate modifiche**
    * La scena è stata salvata in Unity?
    * È stata scelta la piattaforma su cui si sta testando?
    * Sei nel mondo giusto? È stato scelto il modello giusto nel modulo Uploader AND in the World?
    * Sono stati controllate le statistiche della pagina Modello?

**Upload ha esito negativo o si verifica il timeout**
    * L'errore di caricamento più comune è la presenza di una versione di Unity errata. È necessario che corrisponda esattamente alla versione richiesta.
    * Il caricamento potrebbe essere troppo grande. Provare a mantenere le scene del PC < 100 MB. Iniziare in piccolo e creare. Ottimizzare, ottimizzare, ottimizzare.
    * Provare con un nuovo progetto che contiene un cubo semplice.
    * Non forzare l'uscita durante una compilazione: può danneggiare la scena. Provare a ricaricare.

**Si tratta di un processo lento**
    * È consigliabile compilare solo per PC durante l'iterazione e per Android in un secondo momento.
    * Provare a rimuovere i file inutilizzati. Per qualsiasi motivo, Unity talvolta diventa troppo zealous.

**Non è possibile accedere con le credenziali altspace**
    * Per i messaggi di posta elettronica viene fatto distinzione tra maiuscole e minuscole.
    * Provare con un nuovo progetto.
    * Assicurarsi che l'account Altspace sia in regola.

## <a name="see-also"></a>Vedi anche

* [Unity Learn](https://unity3d.com/learn)
* [Forum di Unity](https://forum.unity.com)  
