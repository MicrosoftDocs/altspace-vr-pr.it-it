---
title: Non è possibile avviare AltspaceVR
description: Informazioni su come identificare, segnalare e correggere i problemi relativi all'avvio dell'ambiente AltspaceVR.
ms.date: 02/10/2021
ms.topic: article
keywords: Domande frequenti
ms.openlocfilehash: fc49b5b7ed708e43a12616d782a397a364b2264e
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213131"
---
# <a name="i-cant-launch-altspacevr"></a>Non è possibile avviare AltspaceVR

Esistono diversi motivi per cui non è possibile avviare AltspaceVR. Provare a eseguire i passaggi seguenti per assicurarsi che l'applicazione sia installata correttamente con il software di terze parti necessario.

## <a name="if-youre-trying-to-launch-altspacevr-for-the-first-time"></a>Se si sta provando ad avviare AltspaceVR per la prima volta:

1. Verificare che il dispositivo sia supportato e soddisfi i [requisiti minimi specificati](../getting-started/system-requirements.md).
2. Verificare che sia installato il [software Oculus](https://www.oculus.com/setup) più recente e che Settings-> General-> Unknown Devices sia impostato su on. Se viene avviato in modalità 2D, non è necessario che l'Oculus sia installato.
3. Assicurarsi di disporre di una connessione Internet funzionante. Se si sta provando ad avviare Altspace dall'interno di un firewall di rete, aprire le porte UDP 5055 e 5056 e le porte TCP 80 e 443. Se si è all'interno della rete di un firewall aziendale o didattico, potrebbe essere necessario contattare l'amministratore di rete o il reparto IT.
4. Vedere anche la pagina relativa alla
    * [Installazione di AltspaceVR per Oculus quest](../getting-started/oculus-installation.md)
    * [Installazione di AltspaceVR per la realtà mista di Windows](../getting-started/wmr-installation.md)

## <a name="if-altspacevr-reports-that-the-current-version-is-out-of-date"></a>Se AltspaceVR segnala che la versione corrente non è aggiornata:

* La versione dell'applicazione in uso non è più supportata. Se è stato scaricato AltspaceVR tramite una vetrina, è possibile che l'aggiornamento sia stato avviato di recente prima che l'archivio sia stato in grado di aggiornare il client.
* Se si vuole forzare l'aggiornamento, è possibile eseguire questa operazione tramite le varie vetrine:
    * **Microsoft Store:** [supporto Microsoft Store-ottenere gli aggiornamenti per app e giochi in Microsoft Store](https://support.microsoft.com/account-billing/get-updates-for-apps-and-games-in-microsoft-store-a1fe19c0-532d-ec47-7035-d1c5a1dd464f)
    * **Oculus:** Aprire la libreria Oculus e passare a' aggiornamenti ' nella barra di spostamento a sinistra.
    * **Steam:** [supporto di steam-aggiornamento & problemi di installazione](https://support.steampowered.com/kb_article.php?ref=2274-IFLV-5334)

## <a name="if-the-program-was-working-but-ceased-to-launch-after-update"></a>Se il programma funzionava, ma si è interrotto l'avvio dopo l'aggiornamento:

* Eseguire una "riinstallazione pulita" del software. Per questa operazione è necessario disinstallare o rimuovere le versioni esistenti dell'applicazione. Una volta rimossa completamente dal sistema, installare Altspace tramite Steam, Oculus o Microsoft Store.
* Se si riscontra un problema durante l'avvio di AltspaceVR, è possibile segnalarlo tramite un [ticket di supporto](https://help.altvr.com/hc/requests/new). Includere un [file di log](uploading-client-logs.md) dalla sessione.

## <a name="if-altspacevr-fails-to-launch-after-customizing-your-home-space"></a>Se AltspaceVR non viene avviato dopo la personalizzazione dello spazio Home:

* Passare al [sito Web dello spazio Home](https://account.altvr.com/users/sign_in).
* Verificare che il modello del mondo esista ancora. Se il modello è stato condiviso con l'utente, potrebbe essere stato eliminato dal proprietario, il che potrebbe causare un errore di caricamento dello spazio domestico.
    * Se il modello è stato eliminato, è sufficiente modificare il mondo dal pannello ' strumenti internazionali ' di sinistra, sostituire il modello esistente con un altro modello è Update ' per salvare le modifiche.
* Rimuovere gli oggetti che potrebbero non riuscire a caricare selezionando ' oggetti ' dal pannello ' strumenti internazionali ' sinistro. Gli oggetti problematici possono includere:
    * Oggetti da kit eliminati, o oggetti eliminati da kit, che sono ancora presenti nel mondo.
    * GLTFs sperimentale.
* Dopo aver indirizzato gli elementi precedenti, tentare di immettere nuovamente AltspaceVR.

Il supporto più avanzato per gli amministratori di rete o i reparti IT, inclusi gli intervalli IP e i tag di servizio di Azure, è reperibile nei [Dettagli del download](https://www.microsoft.com/en-us/download/details.aspx?id=56519).