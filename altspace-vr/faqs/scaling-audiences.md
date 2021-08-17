---
title: Ridimensionamento dei destinatari con la funzionalità FrontRow
description: Informazioni su come abilitare, risolvere i problemi e ridimensionare i destinatari altspaceVR con la funzionalità FrontRow.
ms.date: 03/11/2021
ms.topic: article
keywords: ridimensionamento, prima riga
ms.openlocfilehash: 3b6a518a463fc373439f411d4ae75352a0343304b1fb73c8848d3bfd5fa19973
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128067"
---
# <a name="scaling-your-audiences-with-frontrow-feature"></a>Ridimensionamento dei destinatari con la funzionalità FrontRow

## <a name="what-is-frontrow"></a>Che cos'è FrontRow?

FrontRow è una tecnologia AltspaceVR che consente di eseguire il mirroring dell'intero evento in più istanze. FrontRow consente di ridimensionare il pubblico oltre i limiti delle singole camere e può essere usato per ospitare grandi destinatari in un singolo evento. Senza FrontRow, le dimensioni dei destinatari saranno limitate al limite della stanza dell'ambiente principale.

## <a name="how-does-it-work"></a>Come funziona?

FrontRow aggiunge funzionalità e capacità aggiuntive all'esperienza Host, offrendo il massimo controllo sull'evento e sui destinatari. 

* Lo **strumento On-Air** viene aggiunto al pannello host.
    * Con **On-Air** è possibile scegliere chi "rispecchiare" (ad esempio relatori, interpreti, panelist, membri del pubblico e così via) FrontRow "rispecchia" anche il contenuto in tutte le stanze. Pertanto, se si dispone di un pannello di altoparlanti e di una presentazione, è possibile "rispecchiare" gli altoparlanti e la presentazione in tutte le stanze di FrontRow.
* Nel **pannello** guest viene visualizzata una scheda Rooms (Stanze).
    * Questo pannello offre una panoramica a colpo d'occhio del numero di stanze disponibili, del numero di guest presenti in ogni stanza e degli utenti guest. Da qui è anche possibile scegliere Add **Room** (Aggiungi stanza) o **Delete Room** (Elimina stanza) per gestire le dimensioni della configurazione più adatta all'evento.
    * Puoi teletrasportarti da una stanza all'altra e distribuire facilmente i moderatori tra gli spazi.
* Distribuzione reattiva dei destinatari
    * Quando i guest iniziano a immettere lo spazio, FrontRow li distribuirà in modo intuitivo. Può essere configurato per riempire una stanza alla volta o per riempire contemporaneamente più stanze per una distribuzione più uniforme del pubblico.

## <a name="when-to-enable-frontrow"></a>Quando abilitare FrontRow

Eseguire la conversione in FrontRow quando è necessario eseguire la scalabilità oltre la capacità della stanza dell'ambiente.

* Gli ambienti del modello AltspaceVR ufficiale consentono un massimo di 50 avatar per spazio. Se si prevede un pubblico maggiore di 50, usare FrontRow per creare più stanze di 50 avatar.
* Le parole personalizzate (unity uploader/modelli di spazio personalizzati) consentono anche un massimo di 50 avatar per spazio se usati come ambiente eventi. Se si prevede un pubblico maggiore di 50, usare FrontRow per creare più stanze di 30 avatar.

## <a name="how-to-enable-frontrow"></a>Come abilitare FrontRow

1. [Creare l'evento](https://account.altvr.com/events/new).
2. Immettere l'evento.
3. Una volta all'interno dell'evento, **aprire Host Tools (Strumenti host)** nell'angolo inferiore destro.
4. Selezionare il pulsante **Pannello di** partecipazione.
5. Passare alla scheda **Rooms (Stanze)** e da qui è possibile **aggiungere una stanza**
    * Si noti che la generazione di un'altra stanza può richiedere fino a 30 secondi. 
6. Quando la nuova stanza è aperta, verrà visualizzata nella **scheda Rooms (Stanze).** 

## <a name="how-to-use-frontrow"></a>Come usare FrontRow

La conversione dell'evento in un evento FrontRow aggiunge alcuni strumenti e capacità aggiuntivi al pannello host. In particolare, verrà **visualizzata una** scheda Rooms (Stanze). Da questa scheda è possibile:

* **Add Room (Aggiungi** stanza) - Aggiungere una stanza aggiuntiva all'evento. 
* **Elimina stanza:** consente di rimuovere un'intera stanza dall'evento.
* **Reset Space (Reimposta** spazio) - Reimposta la stanza selezionata. In questo modo i guest reim possibile reim inserire lo stesso spazio.
* **Ridistribuire:** ridistribuire tutti i guest attualmente in una stanza in altre stanze. (È un'ottima scelta per il crowding).
* **Teletrasporto:** passare a un'altra stanza.

In un evento FrontRow, gli host visualizzano anche altri strumenti e funzionalità come **On-Air.** Questo pulsante, che si trova accanto a **Host Tools**(Strumenti host), consente a un host o a un moderatore di rispecchiare i membri del gruppo di destinatari e altri partecipanti in modo che possano essere visibili in tutti gli spazi. In qualità di host, è probabile che si voglia essere **anche on-air.** (Pro suggerimento: [Usare zone host](https://altvr.com/holiday2020/) per abilitare automaticamente l'attivazione in modalità on-air per tutti gli utenti all'interno della zona.

Per un'analisi completa e approfondita di ognuna delle funzionalità e delle funzioni disponibili per gli host negli eventi [FrontRow,](../tutorials/host-tools-for-events.md) vedere l'articolo Host Tools Overview for FrontRow Events (Panoramica degli strumenti host per eventi FrontRow).

![Panoramica degli strumenti del pannello host](images/scaling-audiences.png)

Se è necessaria una mano, inviare un ticket al team di supporto [all'altvr.com/eventsupport](https://help.altvr.com/hc/en-us/requests/new?ticket_form_id=360001833313)

* Includere l'URL dell'ID evento (ad esempio: [https://account.altvr.com/events/1461193283454632537](https://account.altvr.com/events/1461193283454632537) )
    * Per ottenerlo, accedere al sito Web www.altvr.com, andare a Eventi/Eventi/Evento personale e copiare l'URL nella barra degli indirizzi del browser o fare clic sul pulsante CONDIVIDI per ottenere l'URL.
    * Ticket-response può richiedere 3-5 giorni lavorativi, quindi inviare la richiesta il più in anticipo possibile.
 
## <a name="how-will-i-know-when-frontrow-is-on"></a>Come è possibile sapere quando FrontRow è on?

Si saprà che l'evento è stato convertito quando si inizia a vedere altre stanze aggiunte alla **scheda** Stanze. Se vuoi 
 
## <a name="can-i-turn-off-frontrow"></a>È possibile disattivare FrontRow?

È possibile. È possibile **eliminare la stanza** con la facilità con cui è possibile aggiungere **spazio.** Il **pulsante Elimina** stanza si trova accanto a ognuna delle stanze nella scheda **Stanze.** Quando si elimina una stanza con persone al suo interno, FrontRow notifica l'eliminazione e la ridistribuisce in altre stanze attive. Ridimensionando l'evento fino a un'unica stanza, è possibile disattivare frontrow in modo efficace. 
 
## <a name="any-pro-tips-or-helpful-hints-to-be-aware-of"></a>Suggerimenti per professionisti o suggerimenti utili da tenere presenti?

La configurazione di un evento dipende da fattori diversi. Anche se non esiste una formula esatta per il successo, ecco alcuni suggerimenti pro e suggerimenti utili per l'hosting di eventi (FrontRow o meno) in AltspaceVR:
* Pensare all'esperienza del pubblico e fare ciò che è possibile ottimizzare per tutti. Ad esempio, se l'ambiente non è semplice da usare per i dispositivi mobili, può traslare l'esperienza di un utente con un visore VR per dispositivi mobili. Per far crescere il pubblico, si vuole fare un'ottima prima impressione.
* La pratica rende perfetti. Prima di ospitare un evento live, eseguire il maggior numero possibile di run-through. Assicurarsi di avere familiarità con tutti gli strumenti a portata di mano, in modo da avere la certezza di essere al primo posto. Se l'evento include talent (speaker/interpreti) anche nei run-through.
* Evitare modifiche dell'ultimo minuto. Può sembrare allettante eliminare un'aggiunta o ridisporre la configurazione dell'evento minuti prima dell'ora di inizio. ma si potrebbe fare clic in modo erto a una modifica che interrompe l'evento. 
* Non dimenticare la moderazione. Esaminare gli strumenti di moderazione (Kick, Report, Block, Mute), assegnare moderatori per tenere sotto controllo gli eventi e condividere le regole dell'evento con i guest. Tenere presente che le persone che non hanno esperienza con la realtà virtuale potrebbero non sapere sempre quali sono le norme sociali delle riunioni virtuali.