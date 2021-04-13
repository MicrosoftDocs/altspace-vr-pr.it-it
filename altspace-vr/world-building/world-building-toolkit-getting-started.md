---
title: Introduzione a World Building Toolkit
description: Informazioni su come configurare e caricare i mondi AltspaceVR usando i modelli di scena Unity con il World Building Toolkit.
ms.date: 03/11/2021
ms.topic: article
keywords: Toolkit
ms.openlocfilehash: cf4660f46d93ca5c5f23de3f567ff04b12519617
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2021
ms.locfileid: "107212625"
---
# <a name="introducing-the-world-building-toolkit"></a>Introduzione a World Building Toolkit

> [!NOTE]
> Il World Building Toolkit è un progetto della community eseguito dal nostro splendido amico, [Anthony Madden](https://twitter.com/chigamesstudio), con supporto da noi. Se si è interessati, partecipare alla [discordia ufficiale di AltspaceVR](https://discordapp.com/invite/altspacevr) e visitare il canale per la creazione di #world. Attualmente abbiamo una versione beta di valutazione Mac, [più dettagli](https://altvr.com/altspacevr-mac)

Il caricatore consente di usare una scena Unity come modello per i mondi. È possibile portare in una casa ospitata per Halloween o la creazione preferita da Minecraft. Se è possibile importarlo in Unity, è possibile che si ottenga in Altspace in questo modo. Di seguito sono riportati alcuni [scenari di esempio](https://account.altvr.com/worlds/1046572460192825569).

![Scenari di esempio](images/unity-uploader-img-01.png)

## <a name="setup"></a>Eseguire la configurazione

1. Unisciti alla [discordia ufficiale di AltspaceVR](https://discordapp.com/invite/altspacevr) e visita il canale per la creazione di #world, non lasciare che gli amici creino solo i mondi.
2. Leggi la nostra guida per la [creazione di introduzione](world-building-getting-started.md) per le nozioni di base
3. [Installare Hub Unity](https://blogs.unity3d.com/2018/01/24/streamline-your-workflow-introducing-unity-hub-beta) e installare **Unity 2019.4.2 F1**. Il caricatore non funzionerà a meno che non si corrisponda esattamente a questa versione. È necessario un account Unity gratuito se non ne è disponibile uno e scegliere **personale** perché si sta eseguendo questa operazione per divertimento. Durante l'installazione, assicurarsi di selezionare l'opzione **compilazioni Android** e disabilitare l'aggiornamento automatico.
4. [Scaricare la versione più recente dell'Uploader Unity](https://aka.ms/AsvrCommunityUploader)
5. [Creare un modello](https://account.altvr.com/space_templates/new) nel sito Web. Denominarlo **Hello World modello**.
6. [Creare un mondo](https://account.altvr.com/worlds/my) e denominarlo **Hello World**. Selezionare **Hello World modello** come modello.

![Schermata del mondo creata](images/unity-uploader-img-02.png)

## <a name="upload-your-scene"></a>Caricare la scena

> [!VIDEO https://channel9.msdn.com/Shows/Docs-Mixed-Reality/How-to-upload-a-Template/player]

1. Aprire Hub Unity e creare un nuovo progetto Unity 2019.4.2 F1.
2. Con il progetto aperto, importare il caricatore facendo doppio clic sul file scaricato (si tratta di un pacchetto Unity). A questo punto verrà visualizzata una nuova scheda denominata **AltspaceVR**. È necessario importare il pacchetto per ogni progetto Unity che si vuole usare con Altspace
3. Aprire il **Menu > AltspaceVR > impostazioni di compilazione**
4. Accedere con le credenziali dell'account Altspace
5. Selezionare **Carica modelli** e quindi selezionare **Hello World modello**
6. Aggiungere un cubo alla scena e salvarlo.
7. Controllare **Compila per Windows?** e deselezionare **Compila per Android?**
8. Selezionare **Carica**. In circa un minuto dovrebbe essere visualizzato il **caricamento** completato.
9. Unisciti a **Hello World** avviando Altspace e immettendo da **menu > Worlds > My Worlds**
10. Reimposta il mondo dal **Menu > impostazioni > modera > Reimposta spazio**
11. Il cubo verrà visualizzato. Se si esegue questa operazione velocemente come nel video precedente, è possibile visualizzare le modifiche entro un minimo di 10 secondi.

## <a name="whats-supported"></a>Attività supportate

* Sì: modelli, collisioni, animazioni, effetti particellari, audio, Skybox e così via
* No: script. Per motivi di sicurezza, i caricamenti contenenti script verranno rifiutati
* Forse: le cose più fantasiose come l'illuminazione globale dinamica
* Caricare scene per diverse piattaforme separatamente o insieme
* Vedi i [mondi in primo piano](https://account.altvr.com/worlds/featured), molti sono stati creati usando l'Uploader

## <a name="tips"></a>Suggerimenti

* Partecipare alla [discordia ufficiale di AltspaceVR](https://discordapp.com/invite/altspacevr).
* Nella pagina modello sul lato sinistro vengono mostrati i caricamenti più recenti per piattaforma. In caso di esito positivo, verrà visualizzato **1-2 minuti fa**. Screen_Shot_2019-01-11 _at_1.21.04_AM.png

![Pannello modelli aperto con caricamenti evidenziati](images/unity-uploader-img-03.png)

* Quando si esegue l'aggiornamento, è possibile essere in tutto il mondo. Nel momento in cui il **caricamento** è stato completato, è possibile reimpostare il mondo per visualizzare le modifiche.
* La compilazione per solo PC con una semplice scena dovrebbe richiedere meno di un minuto per visualizzare una modifica in Altspace
* Impostare il mondo in modo che sia privato e non in elenco per evitare distrazioni.
* Posizionare un cubo nell'origine in modo da visualizzare la posizione in cui le persone genereranno per impostazione predefinita. Nascondere il cubo durante il caricamento.

## <a name="troubleshooting"></a>Risoluzione dei problemi

Sono in **calo o non è possibile teletrasportarsi su nulla** È necessario aggiungere una collisione agli oggetti per teletrasportarsi su di essi.

**Niente modificato**
    * La scena è stata salvata in Unity?
    * Hai scelto la piattaforma su cui stai testando?
    * Sei nel mondo giusto? È stato scelto il modello appropriato nell'Uploader e nel modulo mondiale?
    * Sono state controllate le statistiche della pagina del modello?

**Il caricamento ha esito negativo o scade**
    * L'errore di caricamento più comune è la versione di Unity non corretta. Deve corrispondere esattamente alla versione richiesta.
    * Il caricamento potrebbe essere troppo grande. Provare a lasciare le scene del PC < 100 MB. Avvia Small e compila. Ottimizza, ottimizza, ottimizza.
    * Provare con un nuovo progetto con un semplice cubo.
    * Non forzare l'uscita durante una compilazione. può danneggiare la scena. Provare a ricaricare.

**Si tratta di un processo lento**
    * Si consiglia di compilare per PC solo durante l'iterazione e per Android in un secondo momento.
    * Provare a rimuovere i file inutilizzati. Per qualsiasi motivo, Unity diventa troppo zelante a volte.

**Non riesco ad accedere con le credenziali di Altspace**
    * Le lettere maiuscole
    * Provare con un nuovo progetto.
    * Assicurarsi che l'account Altspace sia in una posizione corretta.

## <a name="see-also"></a>Vedi anche

* [Apprendimento per Unity](https://unity3d.com/learn)
* [Forum di Unity](https://forum.unity.com)
