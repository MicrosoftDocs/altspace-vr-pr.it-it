---
title: Uso del teletrasporto
description: Informazioni su come viaggiare da un evento o un mondo a un altro usando un teletrasporto in AltspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: Teletrasporto
ms.openlocfilehash: 79c5b09e1643a70939ba1e967a948ac6c80c2b615bce9eef598d0e07b7722ea3
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126187"
---
# <a name="using-the-teleporter"></a>Uso del teletrasporto

Il viaggio da un evento o un mondo a un altro è un ottimo modo per te e la community di esplorare tutto ciò che AltspaceVR ha da offrire.

## <a name="the-short-version"></a>Versione breve

![Passaggi di teletrasporto dal pannello dell'editor all'impostazione di una destinazione di teletrasporto](images/teleporter.png)

## <a name="the-slightly-longer-version"></a>Versione leggermente più lunga

Prima di tutto, assicurarsi di essere nel proprio spazio domestico, in un evento o in un mondo in cui è stato creato o in cui è stato assegnato il ruolo Terraformer. Se si è in modalità 2D e non viene visualizzato il pulsante World Editor in basso a destra nell'interfaccia utente, fare clic con il pulsante destro del mouse per attivare/disattivarlo. Se il pulsante World Editor non è ancora visualizzato, è possibile che si sia nello spazio di un altro utente. In questo caso, chiedere all'host di assegnare il ruolo Terraformer.

Sarà utile anche per: 
1. Creare prima gli eventi o i mondi
2. Passare al punto in cui si vuole generare il teletrasporto, in modo che eventi/mondi si popoleranno nel pannello Destinazione teletrasporto e renderanno più veloce e più semplice connetterli.

Un altro trucco per spostarsi con i teletrasportatori in modalità 2D è usare CTRL+BARRA SPAZIATRICE. Verrà visualizzato il prompt dei comandi ed è possibile digitare: back -That will take you back to the last space you were in. 

Passare ora alla posizione in cui si vuole generare un teletrasporto e selezionare World Editor/Editor Panel/Basics/Teleporter.

Verrà visualizzato il pannello Destinazione teletrasporto. Verranno visualizzati tre categorie tra cui scegliere:

* **MY SPACES** : elenco di mondi creati.
* **RECENT:** elenco degli eventi recenti a cui sei stato fatto. Usare questa opzione se si vuole passare a un evento. Questa è l'unica opzione che consente di passare a un evento, gli altri 2 consentono solo di passare da un mondo all'altro. NOTA: vedere Avanzate di seguito se si connettono eventi in prima riga con Mondi importati. Sarà necessario generare e configurare i teletrasportatori nel mondo importato e non nell'evento effettivo.
* **IN PRIMO** PIANO: elenco di mondi in primo piano su cui è possibile impostare il teletrasporto.

Selezionare l'evento o il mondo che si vuole usare, che genera il teletrasporto e mette un testo Etichetta del nome evento o Mondo leggermente indietro. È quindi possibile selezionare l'icona Ingranaggio nella sezione Oggetti presenti per modificare il nome dell'etichetta.

È possibile selezionare teletrasporto con il cursore (verrà chiesto se è ok andare in questo punto, nel caso in cui si sia verificata un'errore di clic) o spostare l'avatar direttamente nel Teleporter e, presto, si sta viaggiando verso la destinazione. Digli di salutare.

## <a name="advanced-features"></a>Funzionalità avanzate

Se si crea una conferenza, un vertice o un evento più grande usando Front Row con un mondo personalizzato (ad esempio, un mondo di base, un modello di spazio del caricatore Unity, Re-Import World), è necessario configurare il teletrasporto nel mondo di base e NON nell'evento effettivo. Assicurarsi di configurare il teletrasporto per il viaggio all'evento corretto (deve essere presente nell'elenco Recenti) in Foundation World, quindi Re-Import World in the Event per far sì che i teletrasportatori siano visualizzati in tutti gli spazi eventi della prima riga.

## <a name="faqs"></a>Domande frequenti

**Errore: "Siamo spiacenti, ma non è possibile consentire l'accesso"**

L'evento potrebbe avere un gruppo associato, quindi solo i nomi utente nel gruppo possono accedere a tale teletrasporto per accedere all'evento del gruppo privato.

**Quanti teletrasportatori è possibile usare in un unico spazio?**

I teletrasportatori usano trame trasparenti con effetti di particelle animate, quindi è consigliabile non avere troppi elementi nello stesso punto/sovrapposizione in quanto ciò potrebbe influire sulle prestazioni. Provare a non avere più di 4 nella stessa area o più di 10 se sono tutte distribuite nello spazio.