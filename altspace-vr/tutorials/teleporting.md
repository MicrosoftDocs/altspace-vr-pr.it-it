---
title: Uso del teletrasporto
description: Informazioni su come andare da un evento o un mondo a un altro usando un teletrasporto in AltspaceVR.
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

Il viaggio da un evento o un mondo a un altro è un ottimo modo per esplorare tutto ciò che AltspaceVR ha da offrire.

## <a name="the-short-version"></a>Versione breve

![Passaggi di teletrasporto dal pannello dell'editor all'impostazione di una destinazione di teletrasporto](images/teleporter.png)

## <a name="the-slightly-longer-version"></a>Versione leggermente più lunga

Prima di tutto, assicurarsi di essere nell'homespace, in un evento o in un mondo creato o in cui è stato assegnato il ruolo Terraformer. Se si è in modalità 2D e il pulsante World Editor non è visualizzato nella parte inferiore destra dell'interfaccia utente, fare clic con il pulsante destro del mouse per attivarlo o disattivarlo. Se il pulsante World Editor (Editor mondo) non è ancora visualizzato, è possibile che si sia nello spazio di un altro utente. In questo caso, chiedere all'host di assegnare il ruolo Terraformer.

Consente anche di: 
1. Creare prima eventi o worlds
2. Passare alla posizione in cui si vuole generare il teletrasporto, in modo che eventi/mondo si popoli nel pannello Destinazione teletrasporto e se ne releni più velocemente e più facilmente la connessione.

Un altro modo per spostarsi con i teletrasportatori in modalità 2D è usare CTRL+BARRA SPAZIATRICE. Verrà visualizzato il prompt dei comandi ed è possibile digitare: back -That will take you back to the last space you were in! 

Passare ora alla posizione in cui si vuole generare un teletrasporto e selezionare World Editor/Editor Panel /Basics/Teleporter (Editor mondo/Pannello editor/Nozioni di base/Teletrasporto).

Verrà visualizzato il pannello Destinazione teletrasporto. Verranno visualizzati tre categorie tra cui scegliere:

* **MY SPACES** : elenco di world creati.
* **RECENTI:** elenco degli eventi recenti a cui si è stati. Usare questa opzione se si vuole passare a un evento. Questa è l'unica opzione che consente di passare a un evento, gli altri 2 consentono solo di passare da un mondo all'altro. NOTA: vedere Avanzate di seguito se si connettono eventi di front-row con scenari importati, sarà necessario generare e configurare i teletrasportatori nell'area importata e non nell'evento effettivo.
* **IN** PRIMO PIANO: elenco di mondo in primo piano su cui è possibile impostare il teletrasporto.

Selezionare l'evento o il mondo che si vuole usare, che genererà il teletrasporto e inserirà un testo Etichetta del nome Evento o Mondo leggermente indietro. È quindi possibile selezionare l'icona a forma di ingranaggio nella sezione Oggetti presenti per modificare il nome dell'etichetta.

È possibile selezionare il teletrasporto con il cursore (verrà chiesto se è possibile farlo, in caso di errore) oppure spostare l'avatar direttamente nel teletrasporto e, presto, si è in viaggio verso la destinazione. Tell them we say hi!

## <a name="advanced-features"></a>Funzionalità avanzate

Se si sta creando una conferenza, un vertice o un evento più ampio usando Front Row con un mondo personalizzato (ad esempio, Foundation World, Unity Uploader Space Template, Re-Import World), è necessario configurare il teletrasporto nel mondo delle fondamenta e NON nell'evento effettivo. Assicurarsi di configurare il teletrasporto per il viaggio verso l'evento corretto (deve essere presente nell'elenco Recenti) in Foundation World, quindi Re-Import World nell'evento per visualizzare i teletrasportatori in tutti gli spazi degli eventi front-row.

## <a name="faqs"></a>Domande frequenti

**Errore: "Sorry, we'd like to, but we just can't let you in there"**

È possibile che all'evento sia associato un gruppo, quindi solo i nomi utente nel gruppo possono accedere a tale teletrasporto per accedere all'evento del gruppo privato.

**Quanti teletrasportatori è possibile usare in un unico spazio?**

I teletrasportatori usano trame trasparenti con effetti di particelle animate, quindi è consigliabile non avere troppi elementi nella stessa posizione/sovrapposizione perché ciò potrebbe influire sulle prestazioni. Provare a non avere più di 4 nella stessa area o più di 10 se sono tutti distribuiti nello spazio.