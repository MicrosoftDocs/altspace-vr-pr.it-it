---
title: Uso del proiettore Web per lo streaming di un browser
description: Informazioni su come usare il proiettore Web per trasmettere il contenuto da un browser designato in esperienze AltspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: proiettore Web, flusso, browser
ms.openlocfilehash: 8f25de68ba633e10b9192b85c883de4ba48fd7987ec5d301ebac8443982a1a55
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119127309"
---
# <a name="using-the-web-projector-to-stream-a-browser"></a>Uso del proiettore Web per lo streaming di un browser

Il proiettore Web AltspaceVR è una soluzione di condivisione multimediale affidabile che consente di trasmettere una scheda del browser designata dal PC desktop direttamente ad AltspaceVR. Può essere usato per condividere diapositive, video, foto e qualsiasi altro elemento che è possibile aprire da un browser.* Il proiettore Web richiede il download di un'estensione del browser ed è attualmente disponibile esclusivamente tramite World Editor. Di seguito è riportata una panoramica completa della funzionalità e di come usarla:

## <a name="requirements"></a>Requisiti

1. Per eseguire lo streaming del browser, è necessario usare un PC o Mac.
2. L'estensione del browser necessaria è attualmente supportata dal browser Microsoft Edge. Stiamo lavorando per espandere questo elenco.
3. Anche se è possibile trasmettere da un computer Mac, il proiettore Web non è ancora disponibile nel client Mac AltspaceVR.
4. Se tutto è configurato correttamente (connesso all'estensione del browser/AltspaceVR con lo stesso account, connesso/trasmesso con il proiettore Web in AltspaceVR) e viene ancora visualizzata una schermata verde, WebProjector richiede la porta TCP 443 aperta e l'intervallo di porte UDP 20000-20400.

> [!NOTE]
> Questa funzionalità è destinata principalmente a trasmettere in streaming una scheda del browser di propria scelta. Se si sta invece tentando di trasmettere in streaming l'applicazione desktop, il proiettore Web trasmettere tutto l'audio del computer (incluso AltspaceVR) che può comportare echo/feedback. Per evitare che ciò accada, è necessario disattivare AltspaceVR. In alternativa, è anche possibile usare un dispositivo separato per eseguire AltspaceVR durante lo streaming dal PC.

## <a name="getting-started"></a>Introduzione

1. Per iniziare, è necessario scaricare e installare l'estensione del browser, disponibile [qui](https://account.altvr.com/web_projector).
2. Successivamente, [sideload dell'estensione nel browser Microsoft Edge.](https://docs.microsoft.com/microsoft-edge/extensions-chromium/getting-started/extension-sideloading)
    * Al termine del download, passare alla **sezione Estensioni** del browser. (Disponibile in **Impostazioni**)
    * Decomprimere il file .zip.
    * Attivare la **modalità sviluppatore** e selezionare **Carica disimballato**
    * Scegliere la cartella appena decompressa. Questa è l'estensione del proiettore Web.
    * Dopo aver aggiunto l'estensione, è possibile passare a **Dettagli** per configurare le impostazioni.

## <a name="setting-up-a-shareable-browser"></a>Configurazione di un browser condivisibile

Dopo aver scaricato e installato l'estensione, è possibile usarla.

1. Aprire una scheda nel browser Microsoft Edge e passare ai file multimediali che si desidera condividere.
2. Configurare la finestra in modo da essere pronti per la condivisione. (Nota: l'intera finestra del browser verrà proiettata nel mondo)
3. Individuare l'estensione appena installata (visualizzata come icona altspaceVR accanto alla barra dell'URL nel browser). Selezionare ALTSPACEVR. Verrà richiesto di accedere al proprio account. (*Nota: è importante accedere allo stesso account che si userà per configurare il proiettore Web.
4. Dopo aver eseguito l'accesso, nella schermata dell'estensione verrà visualizzata l'opzione **Avvia** streaming. Selezionarla.

## <a name="projecting-your-browser-in-world"></a>Proiettare il browser nel mondo

1. Dopo aver configurato il browser per la proiezione e aver avviato lo streaming tramite l'estensione, aprire AltspaceVR.
2. Configurare il proiettore Web nell'ambiente preferito aprendo World Editor > Basics > Web Projector (Informazioni di base sul web projector)
3. Una volta posizionati, è possibile usare i controlli World Editor per ridimensionare il proiettore Web. Includerà anche istruzioni sullo schermo.
4. Selezionare il **pulsante Connessione** per avviare lo streaming del browser Edge.
5. Ricordarsi di **fare clic su** Broadcast per iniziare a condividere con tutti gli utenti guest nello spazio.
6. Non dimenticare di **arrestare lo streaming.** Alla fine la sessione si timeout, ma fino ad allora continuerà a proiettare il browser in tempo reale. Al termine, è meglio terminare la sessione.

![Browser proiettato in AltspaceVR world](images/web-project-img-01.png)

**Suggerimento per lo streaming di video:** Se si verificano stutter video, arrestare lo streaming, regolare la qualità video su 480p o 360p, quindi riavviare lo streaming e la trasmissione. Risoluzioni più elevate possono richiedere un utilizzo eccessivo della CPU e della larghezza di banda di caricamento.

> [!NOTE]
> Al momento i pulsanti di controllo aggiuntivi nella parte superiore del proiettore Web non sono ancora live. Rimarranno grigie e non selezionabili con il pulsante destro del mouse. Non si tratta di un bug, ma di progettazione (per il momento).

> [!IMPORTANT]
> DISCLAIMER: Nota: l'utilizzo del proiettore Web, come tutte le [](../community/terms-of-service.md) altre funzionalità di AltspaceVR, è soggetto alle Condizioni per l'utilizzo e agli [standard Community Microsoft.](../community/community-standards.md) Di conseguenza, il proiettore Web non può essere usato per lo streaming di contenuto che viola uno dei due contratti. In questo modo verranno eseguite azioni di moderazione da AltspaceVR. L'accesso a Web Projector Open Beta non è garantito e può essere concesso solo per una versione di valutazione temporanea. La lunghezza della versione beta e la durata della partecipazione sono a discrezione del team altspaceVR. L'uso della versione beta del proiettore Web non è obbligatorio e la partecipazione alla versione beta è puramente volontaria. I partecipanti sono invitati a offrire commenti e suggerimenti sul proiettore Web che consentono di modellare le funzionalità e l'usabilità della funzionalità man mano che lo sviluppo continua. La versione beta del proiettore Web può avere funzionalità limitate e potrebbe essere soggetta a bug imprevisti. Grazie, in anticipo, per la partecipazione.
