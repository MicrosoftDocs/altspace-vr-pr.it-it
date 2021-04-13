---
title: Uso del proiettore Web per lo streaming di un browser
description: Informazioni su come usare il proiettore Web per trasmettere contenuto da un browser designato a esperienze AltspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: proiettore Web, flusso, browser
ms.openlocfilehash: 4f89757a572ae3d77a7b11f068760268a4089ddd
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2021
ms.locfileid: "107212841"
---
# <a name="using-the-web-projector-to-stream-a-browser"></a>Uso del proiettore Web per lo streaming di un browser

Il proiettore Web AltspaceVR è una solida soluzione di condivisione multimediale che consente di trasmettere una scheda del browser designata dal PC desktop direttamente in AltspaceVR. Può essere usato per condividere diapositive, video, foto e qualsiasi altra cosa che è possibile aprire da un browser. * il proiettore Web richiede il download di un'estensione del browser ed è attualmente disponibile esclusivamente tramite l'editor di tutto il mondo. Di seguito è riportata una panoramica completa della funzionalità e della relativa modalità di utilizzo:

## <a name="requirements"></a>Requisiti

1. Per eseguire lo streaming del browser è necessario usare un PC o Mac.
2. L'estensione del browser necessaria è attualmente supportata dal browser Microsoft Edge. (Stiamo lavorando per espandere questo elenco).
3. Sebbene sia possibile trasmettere da un computer Mac, il proiettore Web non è ancora disponibile nel client Mac di AltspaceVR.

> [!NOTE]
> Questa funzionalità è destinata principalmente a trasmettere una scheda del browser a scelta. Se si sta tentando di trasmettere il flusso dell'applicazione desktop, il proiettore Web eseguirà lo streaming di tutti i file audio del computer (incluso AltspaceVR) che possono generare eco/feedback. Per evitare che ciò accada, è necessario disattivare il AltspaceVR. In alternativa, è anche possibile usare un dispositivo separato per eseguire AltspaceVR mentre si esegue il flusso dal PC.

## <a name="getting-started"></a>Introduzione

1. Per iniziare, è necessario scaricare e installare l'estensione del browser, disponibile [qui](https://account.altvr.com/web_projector).
2. Successivamente, [sideload l'estensione nel browser Microsoft Edge](https://docs.microsoft.com/microsoft-edge/extensions-chromium/getting-started/extension-sideloading).
    * Al termine del download, passare alla sezione **estensioni** del browser. (Disponibile in **Impostazioni**)
    * Decomprimere il file zip.
    * Attiva/Nascondi in **modalità sviluppatore** e seleziona **carica decompresso**
    * Scegliere la cartella appena decompressa. Si tratta dell'estensione del proiettore Web.
    * Una volta aggiunta l'estensione, è possibile visualizzare **i dettagli** per configurare le impostazioni.

## <a name="setting-up-a-shareable-browser"></a>Configurazione di un browser condivisibile

Dopo aver scaricato e installato l'estensione, è possibile usarla.

1. Aprire una scheda nel browser Edge e passare al supporto che si vuole condividere.
2. Configurare la finestra in modo da essere pronti per la condivisione. Nota: l'intera finestra del browser verrà proiettata in tutto il mondo.
3. Individuare l'estensione appena installata (visualizzata come icona AltspaceVR accanto alla barra URL nel browser). Selezionare AltspaceVR. Verrà richiesto di accedere all'account. (* Nota: è importante accedere allo stesso account che verrà usato per configurare il proiettore Web.)
4. Una volta effettuato l'accesso, verrà visualizzata la schermata Extension per offrire un'opzione di **avvio del flusso** . Selezionarla.

## <a name="projecting-your-browser-in-world"></a>Proiezione del browser nel mondo

1. Quando il browser è configurato per la proiezione ed è stato avviato il flusso tramite l'estensione, aprire AltspaceVR.
2. Configurare il proiettore Web nell'ambiente scelto aprendo l'editor del mondo > nozioni di base > proiettore Web
3. Una volta posizionati, è possibile usare i controlli dell'editor del mondo per ridimensionare il proiettore Web. Includerà anche istruzioni, sullo schermo.
4. Selezionare il pulsante **Connetti** per avviare lo streaming del browser Microsoft Edge.
5. Ricordarsi di fare clic su **broadcast** per iniziare la condivisione con tutti i Guest nello spazio.
6. Non dimenticare di **arrestare lo streaming.** Si verificherà un timeout della sessione, ma fino ad allora continuerà a proiettare in diretta il browser. È preferibile terminare la sessione non appena si è finito.

![Browser proiettato in AltspaceVR World](images/web-project-img-01.png)

**Video-suggerimento di streaming:** Se la balbuzie video, interrompere lo streaming, modificare la qualità del video in 480p o 360p, quindi riavviare il flusso e trasmettere la trasmissione. Una risoluzione più elevata può limitare la CPU e caricare la larghezza di banda.

> [!NOTE]
> Al momento i pulsanti di controllo aggiuntivi nella parte superiore del proiettore Web non sono ancora attivi. Rimarranno in grigio e non selezionabili. Non si tratta di un bug, che è da progettazione (per il momento).

> [!IMPORTANT]
> Dichiarazione di non responsabilità: l'utilizzo del proiettore Web, come tutte le altre funzionalità di AltspaceVR, è soggetto alle condizioni per il [servizio](../community/terms-of-service.md) e [agli standard della community](../community/community-standards.md). Di conseguenza, il proiettore Web potrebbe non essere usato per trasmettere il contenuto in violazione di uno dei due contratti. Questa operazione comporterà azioni di moderazione eseguite da AltspaceVR. L'accesso alla versione beta del proiettore Web non è garantito e può essere concesso solo per una versione di valutazione temporanea. La lunghezza della versione beta e la durata della partecipazione sono a discrezione del team AltspaceVR. L'uso della versione beta del proiettore Web non è obbligatorio e la partecipazione alla versione beta è puramente volontaria. I partecipanti sono invitati a offrire commenti e suggerimenti sul proiettore Web che consentiranno di definire la funzionalità e l'usabilità della funzionalità quando lo sviluppo continuerà. La versione beta del proiettore Web potrebbe avere funzionalità limitate e potrebbe essere soggetta a bug imprevisti. Grazie, in anticipo, per la tua partecipazione.
