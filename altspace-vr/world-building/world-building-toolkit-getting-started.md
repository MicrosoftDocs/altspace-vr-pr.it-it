---
title: Introduzione a World Building Toolkit
description: Informazioni su come configurare e caricare gli scenari AltspaceVR usando i modelli di scena Unity con World Building Toolkit.
ms.date: 03/11/2021
ms.topic: article
keywords: Toolkit
ms.openlocfilehash: 8b66e35509060e00b2e52d3770380d009d7060339003f534d23fdd47372a57f0
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119125407"
---
# <a name="introducing-the-world-building-toolkit"></a>Introduzione a World Building Toolkit

> [!NOTE]
> The World Building Toolkit è un progetto della community gestito dal nostro straordinario [amico, Antonio Madden,](https://twitter.com/chigamesstudio)con il supporto di Microsoft. Se si è interessati, partecipare al [discord altspaceVR](https://discordapp.com/invite/altspacevr) ufficiale e visitare il canale #world-building. Al momento è disponibile una versione beta della versione di valutazione Mac. [Altri dettagli](https://altvr.com/altspacevr-mac)

Uploader consente di usare una scena unity come modello per i propri scenari. È possibile ospitare una casa infestata per Il Mio o la propria creazione preferita da Minecraft. Se è possibile importarlo in Unity, è probabile che sia possibile ottenerlo in Altspace in questo modo. Ecco alcuni esempi [di Worlds](https://account.altvr.com/worlds/1046572460192825569).

![Mondo di esempio](images/unity-uploader-img-01.png)

## <a name="setup"></a>Eseguire la configurazione

1. Partecipa al [discord altspaceVR](https://discordapp.com/invite/altspacevr) ufficiale e visita il canale #world-building- Friends don't let friends build Worlds alone (Amici non lasciare che gli amici costruiscono worlds da soli).
2. Per le [nozioni di base, Attività iniziali guida](world-building-getting-started.md) alla creazione del mondo
3. [Installare Unity Hub](https://blogs.unity3d.com/2018/01/24/streamline-your-workflow-introducing-unity-hub-beta) e **Unity 2020.3.9.** Uploader non funzionerà a meno che non si corrisponda esattamente a questa versione. Se non si ha un account Unity gratuito, è necessario scegliere **Personal** (Personale) perché si tratta di un'operazione divertente. Durante l'installazione, assicurarsi di selezionare **l'opzione Compilazioni Android** e disabilitare l'aggiornamento automatico.
4. [Scaricare la versione più recente di Unity Uploader](upgrading-content-to-the-latest-unity.md#altspacevr-uploader-v090-upgrade-guide)
5. [Creare un modello](https://account.altvr.com/space_templates/new) nel sito Web. Assegnare al **Hello World il nome Template**.
6. [Creare un oggetto World](https://account.altvr.com/worlds/my) e deno assegnare **Hello World**. Selezionare **Hello World modello** come Modello.

![Schermata Del mondo creato](images/unity-uploader-img-02.png)

## <a name="upload-your-scene"></a>Upload la scena

> [!VIDEO https://channel9.msdn.com/Shows/Docs-Mixed-Reality/How-to-upload-a-Template/player]

1. Aprire Unity Hub e creare un nuovo progetto Unity 2020.3.9.
2. Con il progetto aperto, importare il caricatore facendo doppio clic sul file scaricato (si tratta di un pacchetto Unity). Verrà ora visualizzata una nuova scheda denominata **AltspaceVR.** È necessario importare il pacchetto per ogni progetto Unity che si vuole usare con Altspace
3. Aprire **il menu > altspaceVR > build Impostazioni**
4. Accedere con le credenziali dell'account Altspace
5. Selezionare **Carica modelli** e quindi selezionare Hello World **modello**
6. Aggiungere un cubo alla scena e salvare.
7. Selezionare **Compila per Windows?** e deselezionare **Compila per Android?**
8. Selezionare **Carica**. Dopo circa un minuto verrà visualizzato **il** Upload completato.
9. Partecipare **Hello World** avviare Altspace ed eseguire l'immissione da **Menu > Worlds > My Worlds**
10. Reset the World from **Menu > Impostazioni > Moderate > Reset Space**
11. Verrà visualizzato il cubo. Se si fa velocemente come nel video precedente, è possibile visualizzare le modifiche entro un massimo di 10 secondi.

## <a name="whats-supported"></a>Attività supportate

* Sì: modelli, collisioni, animazioni, effetti particella, audio, skybox e così via
* No: script. Per motivi di sicurezza, i caricamenti contenenti script verranno rifiutati
* Forse: qualcosa di speciale come l'illuminazione globale dinamica
* Upload scene per piattaforme diverse separatamente o insieme
* Vedere [Featured Worlds (Mondo in](https://account.altvr.com/worlds/featured)primo piano), molti sono stati creati con Uploader

## <a name="tips"></a>Suggerimenti

* Partecipare alla [discord di AltspaceVR ufficiale.](https://discordapp.com/invite/altspacevr)
* Nella pagina Modello sul lato sinistro vengono visualizzati i caricamenti più recenti in base alla piattaforma. Se l'operazione ha avuto esito positivo, **vengono visualizzati 1-2 minuti fa.** Screen_Shot_2019-01-11 _at_1.21.04_AM.png

![Pannello Modelli aperto con i caricamenti evidenziati](images/unity-uploader-img-03.png)

* È possibile essere nel mondo quando si esegue l'aggiornamento. Nel momento in cui il caricatore **Upload completa,** è possibile reimpostare Il mondo per visualizzare le modifiche.
* La creazione solo per PC con una scena semplice dovrebbe richiedere meno di 1 minuto per visualizzare una modifica in Altspace
* Imposta World su Private (Privato) e Unlisted (Non in elenco) per evitare distrazioni.
* Posizionare un cubo all'origine in modo che sia possibile vedere dove verranno generati gli utenti per impostazione predefinita. Nascondere il cubo durante il caricamento.

## <a name="troubleshooting"></a>Risoluzione dei problemi

**I'm falling or can't teleport onto anything** È necessario aggiungere collisioni agli oggetti per teletrasportarli.

**Non sono state modificate modifiche**
    * La scena è stata salvata in Unity?
    * È stata scelta la piattaforma su cui si sta testando?
    * Sei nel mondo giusto? È stato scelto il modello giusto nel modulo Uploader AND in the World?
    * Sono stati controllate le statistiche della pagina Modello?

**Upload ha esito negativo o si verifica il timeout**
    * L'errore di caricamento più comune è la versione di Unity errata. Deve corrispondere esattamente alla versione richiesta.
    * Il caricamento potrebbe essere troppo grande. Provare a mantenere le scene del PC < 100 MB. Iniziare in piccolo e creare. Ottimizzare, ottimizzare, ottimizzare.
    * Provare con un nuovo progetto con un cubo semplice.
    * Non forzare l'uscita durante una compilazione: può danneggiare la scena. Provare a ricaricare.

**Si tratta di un processo lento**
    * È consigliabile compilare solo per PC durante l'iterazione e per Android in un secondo momento.
    * Provare a rimuovere i file inutilizzati. Per qualsiasi motivo Unity talvolta diventa troppo zealous.

**Non è possibile accedere con le credenziali altspace**
    * Per i messaggi di posta elettronica viene fatto distinzione tra maiuscole e minuscole.
    * Provare con un nuovo progetto.
    * Assicurarsi che l'account Altspace sia in regola.

## <a name="see-also"></a>Vedi anche

* [Unity Learn](https://unity3d.com/learn)
* [Forum di Unity](https://forum.unity.com)
