---
title: Uso del teleportatore
description: Informazioni su come spostarsi da un evento o un mondo a un altro usando un teleportatore in AltspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: teletrasporto
ms.openlocfilehash: afc199e958824bb5f0a9ff6d74865cbcd3f16868
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213420"
---
# <a name="using-the-teleporter"></a>Uso del teleportatore

Viaggiare da un evento o da un mondo a un altro è un ottimo modo per consentire all'utente e alla community di esplorare tutto il contenuto di AltspaceVR.

## <a name="the-short-version"></a>Versione breve

![Passaggi di Teleporting dal pannello dell'editor per impostare una destinazione di teleportazione](images/teleporter.png)

## <a name="the-slightly-longer-version"></a>Versione leggermente più lunga

Prima di tutto, assicurarsi di trovarsi nella HomeSpace, in un evento o in un mondo in cui è stato creato o che è stato assegnato il ruolo di bonifica in. Se ci si trova in modalità 2D e il pulsante editor globale non viene visualizzato nella parte inferiore destra dell'interfaccia utente, fare clic con il pulsante destro del mouse su di esso per attivarlo o disattivarlo. Se il pulsante editor globale non è ancora visualizzato, è possibile che si trovi nello spazio di un altro utente. In tal caso, è necessario richiedere all'host di fornire il ruolo di deformatore.

Consente inoltre di: 
1. Creare prima gli eventi o i mondi
2. Passare alla posizione in cui si desidera generare il teleportatore, in modo che gli eventi e i mondi vengano inseriti nel pannello destinazione teleportator e risultino più veloci e facili da connettere.

Un altro espediente che consente di spostarsi con i teleportatori in modalità 2D consiste nell'usare CTRL + barra spaziatrice. Verrà visualizzata la finestra del prompt dei comandi ed è possibile digitare: back, che consente di tornare all'ultimo spazio in cui si trovava. 

Ora passare al percorso in cui si vuole generare un teleportatore e selezionare on editor globale/pannello Editor/nozioni di base/Teleporter.

Verrà impostato il pannello destinazione teleportatore. Verranno visualizzate tre categorie tra cui scegliere:

* **My Spaces** : elenco di mondi creati dall'utente.
* Elenco **recente** degli eventi recenti. Usare questa opzione se si vuole viaggiare a un evento, questa è l'unica opzione che consente di passare a un evento. gli altri 2 consentono solo di spostarsi tra i mondi. Nota: se si connettono eventi di riga in cui sono stati importati, è necessario generare e configurare i teleportatori nel mondo importato e non nell'evento effettivo.
* In **primo piano** : elenco di mondi in primo piano in cui è possibile impostare il teleportatore.

Selezionare l'evento o il mondo che si vuole usare per generare il teleportatore e inserire un'etichetta di testo dell'evento o del nome del mondo leggermente indietro. È quindi possibile selezionare l'icona a forma di ingranaggio nella sezione oggetti attuali per modificare il nome dell'etichetta.

È possibile selezionare sul teleportatore con il cursore (verrà chiesto se è OK, se è stato fatto clic con il pulsante destro del mouse) o spostare l'avatar direttamente nel teleportatore e, presto, si sta viaggiando alla destinazione. Pronunciare gli elementi Hi!

## <a name="advanced-features"></a>Funzionalità avanzate

Se crei una conferenza, un Summit o un evento più grande usando la riga anteriore con un mondo personalizzato, ad esempio un mondo di base, un modello di spazio per l'Uploader Unity, Re-Import mondo, dovrai configurare il teleportatore nel mondo di fondazione e non nell'evento effettivo. Assicurarsi di configurare il teleportatore per passare all'evento corretto (deve provenire dall'elenco recente) nel mondo di fondazione, quindi Re-Import mondo nell'evento per far sì che i teleportari vengano visualizzati in tutti gli spazi degli eventi di riga anteriore.

## <a name="faqs"></a>Domande frequenti

**Errore:' Spiacente, ci piacerebbe, ma non è possibile consentirci**

All'evento potrebbe essere associato un gruppo, pertanto solo i nomi utente del gruppo possono accedere a tale teleportatore per accedere a tale evento del gruppo privato.

**Quanti teleportatori è possibile usare in uno spazio?**

I teleportatori utilizzano trame trasparenti con effetti particellari animati, pertanto è preferibile non avere troppi tutti nella stessa posizione o sovrapposizione che potrebbero influire sulle prestazioni. Provare a non avere più di 4 nella stessa area o più di 10 se sono tutti distribuiti nello spazio.