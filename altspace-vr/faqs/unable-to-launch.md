---
title: Non è possibile avviare AltspaceVR
description: Informazioni su come identificare, segnalare e risolvere eventuali problemi relativi all'avvio dell'ambiente AltspaceVR.
ms.date: 02/10/2021
ms.topic: article
keywords: Domande frequenti
ms.openlocfilehash: 50edddef669aca14640fd6e910c12c15864cf46a099e54bceed40494e9817de4
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119127930"
---
# <a name="i-cant-launch-altspacevr"></a>Non è possibile avviare AltspaceVR

Esistono diversi motivi per cui AltspaceVR potrebbe non essere avviato per l'utente. Provare i passaggi seguenti per assicurarsi che l'applicazione sia installata correttamente con il software di terze parti necessario.

## <a name="if-youre-trying-to-launch-altspacevr-for-the-first-time"></a>Se si sta tentando di avviare AltspaceVR per la prima volta:

1. Verificare che il dispositivo sia supportato e soddisfi i [requisiti minimi specificati.](../getting-started/system-requirements.md)
2. Assicurarsi di avere installato la versione più recente di [Oculus Software](https://www.oculus.com/setup) e che Impostazioni-> General-> Unknown Devices sia impostato su ON. Se si avvia in modalità 2D, Oculus non è necessario installato.
3. Assicurarsi di avere una connessione Internet funzionante. Se si sta tentando di avviare Altspace dall'interno di un firewall di rete, aprire le porte UDP 5055 e 5056 e le porte TCP 80 e 443. Se si è all'interno della rete di un firewall aziendale o didattico, potrebbe essere necessario contattare l'amministratore di rete o il reparto IT.
4. Vedere anche la pagina relativa alla
    * [Installazione di AltspaceVR per Oculus Quest](../getting-started/oculus-installation.md)
    * [Installazione di AltspaceVR per Windows Mixed Reality](../getting-started/wmr-installation.md)

## <a name="if-altspacevr-reports-that-the-current-version-is-out-of-date"></a>Se AltspaceVR segnala che la versione corrente non è aggiornata:

* La versione dell'applicazione in uso non è più supportata. Se AltspaceVR è stato scaricato tramite una vetrina, l'aggiornamento potrebbe essere stato avviato di recente prima che il negozio fosse in grado di aggiornare il client.
* Se si vuole forzare l'aggiornamento, è possibile farlo tramite le varie vetrine:
    * **Microsoft Store:** [Microsoft Store supporto tecnico - Ottenere aggiornamenti per app](https://support.microsoft.com/account-billing/get-updates-for-apps-and-games-in-microsoft-store-a1fe19c0-532d-ec47-7035-d1c5a1dd464f) e giochi in Microsoft Store
    * **Oculus:** Aprire oculus Library e passare a "Updates" (Aggiornamenti) nella barra di spostamento a sinistra.
    * **Problemi di installazione** dell'& di [Vapore: Supporto di Steam](https://support.steampowered.com/kb_article.php?ref=2274-IFLV-5334)

## <a name="if-the-program-was-working-but-ceased-to-launch-after-update"></a>Se il programma funzionava, ma ha smesso di essere avviato dopo l'aggiornamento:

* Eseguire una "reinstallazione pulita" del software. A questo scopo è necessario disinstallare o rimuovere le versioni esistenti dell'applicazione. Dopo la rimozione completa dal sistema, installare Altspace tramite Steam, Oculus o Microsoft Store.
* Se si verifica un problema durante l'avvio di AltspaceVR, è possibile contattarci tramite un [ticket di supporto.](https://help.altvr.com/hc/requests/new) Includere un [file di log](uploading-client-logs.md) dalla sessione.

## <a name="if-altspacevr-fails-to-launch-after-customizing-your-home-space"></a>Se AltspaceVR non viene avviato dopo la personalizzazione dello spazio iniziale:

* Passare al sito [Web dello spazio principale.](https://account.altvr.com/users/sign_in)
* Verificare che il modello del mondo esista ancora. Se il modello è stato condiviso con l'utente, potrebbe essere stato eliminato dal proprietario, causando il caricamento dello spazio di casa.
    * Se il modello è stato eliminato, è sufficiente "Modificare" il mondo nel pannello "World Tools" a sinistra, sostituire il modello esistente con un altro modello e "Update" per salvare le modifiche.
* Rimuovere tutti gli oggetti che potrebbero non essere caricati selezionando "Oggetti" nel pannello "World Tools" a sinistra. Gli oggetti problematici possono includere:
    * Oggetti dai kit eliminati, o oggetti eliminati dai kit, che sono ancora presenti nel mondo.
    * GLTF sperimentali.
* Dopo aver indirizzato gli elementi precedenti, provare a reenter AltspaceVR.

Il supporto più avanzato per gli amministratori di rete o i reparti IT, inclusi gli intervalli IP di Azure e i tag di servizio, è disponibile nei dettagli [del download.](https://www.microsoft.com/en-us/download/details.aspx?id=56519)