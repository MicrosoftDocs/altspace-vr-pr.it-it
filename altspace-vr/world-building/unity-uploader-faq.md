---
title: Guida di Unity Uploader
description: Rimanere aggiornati sulle domande frequenti più recenti e sulle soluzioni per AltspaceVR Unity Uploader.
ms.date: 02/10/2021
ms.topic: article
keywords: guida, domande frequenti
ms.openlocfilehash: cb983ba4e23186f7cc62043f75e7ea1b2969e92b6bd30b132f1733b5e25e92dd
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119125697"
---
# <a name="unity-uploader-help"></a>Guida di Unity Uploader

**1. Quanto è straordinario questo strumento?**

> [!VIDEO https://channel9.msdn.com/Shows/Docs-Mixed-Reality/cheyenne-mountain-gate-room-v1/player]

Questa è la scena di Stargate Unity con un'app SDK che alimentazione gate e DND

**2. I'm a video learner, where's my videos?**

[Guardare i video](https://youtu.be/km9CnVYPzoM)

**3. Dove è possibile trovare esempi?**

[Gli esempi di Worlds](https://account.altvr.com/worlds/featured) [e Jimmy in](https://account.altvr.com/worlds/1046572460192825569) primo piano sono ottimi punti di partenza

**4. Funziona con i kit e il nuovo SDK?**
Sì, è possibile usare tutti gli strumenti insieme, se si desidera. Stiamo provando a svilupparli per lavorare senza problemi insieme.

**5. Supporta gli effetti di particelle?**

![GIF degli effetti delle particelle di snow](images/uploader-faq-img-01.gif)

**6. È possibile ottenere audio spazializzato?**
Non al momento, ma è possibile posizionare le origini audio per la riproduzione in aree localizzate. 

**7. L'illuminazione baked funziona?**
Sì, ma le luci devono essere impostate su "baked" e non "miste"

**8. L'illuminazione globale funziona?**
Sì

**9. È sempre necessario reimpostare il mondo?**
Sì. È necessario ricaricare i bundle di asset Unity ogni volta. 

**10. È possibile usare materiali e shader personalizzati?**

![GIF di materiali e shader personalizzati](images/uploader-faq-img-02.gif)

**11. È possibile eseguire il caricamento in una sola piattaforma?**
Sì, usando lo strumento di caricamento. Tuttavia, gli utenti che sono in Android non vedono nulla nel mondo fino a quando non si carica la scena per la piattaforma. 

**12. Gli script sono consentiti?**
No, per motivi di sicurezza non è possibile consentire script o riferimenti a script. Se il caricamento contiene script o riferimenti a script, verrà rifiutato. Esaminare il nuovo SDK se è necessario creare script. 

**13. Quanto è possibile caricare una scena?**
È consigliabile iniziare con una piccola quantità di dati e fare attenzione alle persone di Altspace che non hanno PC di tipo". Detto questo, abbiamo avuto giochi che hanno portato le proprie mappe per i flussi live (ad esempio, Onward, un gioco di realtà virtuale)

![Screenshot del gioco vr in AltspaceVR](images/uploader-faq-img-03.png)

**14. È necessario ospitare i file della scena?**
No, Altspace sta servendo i file dopo averli caricati

**15. Le ombreggiature sono consentite?**
Sì

**16. Con quale rapidità è possibile eseguire l'iterazione usando lo strumento di caricamento?**
Se si è già nel mondo, è possibile premere Upload in Uploader, reimpostare Il mondo e visualizzare la scena aggiornata in meno di 10 secondi. In genere, vengono visualizzati cicli da 30 secondi a pochi minuti a seconda della complessità della scena. Bevi una bevanda e ti disderti di essere un World Builder.

**17. Dove si ottengono i modelli 3D?**
Sketchfab, Sketchup, Minecraft, Unity Asset Store e così via.

**18. Supporta le animazioni?**

![GIF delle animazioni personalizzate in esecuzione](images/uploader-faq-img-04.gif)

**19. Come è possibile configurare l'audio spaziale?** Importare il file wav preferito, creare un oggetto gioco vuoto nella scena e selezionare questo oggetto. Trascinare e rilasciare il suono importato nel controllo dell'oggetto per creare un'origine audio. Successivamente, regolare il volume su un valore non superiore a 0,5, modificare la fusione spaziale in 3D e regolare la distanza minima e massima per creare un'area audio appropriata. Questa viene visualizzata come sfera come collisori per impostazione predefinita. Per ottenere un calo reale, è necessario modificare la curva di discesa in base alle proprie necessità. [(tramite @IsThatToasted )](https://www.youtube.com/watch?v=ktb2vAAwknw&list=PLGmYIROty-5bpzKQNK3mRMi4pmh_LinV4&t=642s&index=29)

**20. Com'è possibile che si vedano gli occhi incrociati o l'insodenza?**
In alcuni casi uploader non esegue correttamente l'override delle impostazioni di rendering. "Vai a Modifica > Project Impostazioni > lettore". Assicurarsi che "XR Impostazioni > Virtual Reality Supported" (XR Impostazioni > Virtual Reality Supported) sia selezionato e che "Stereo Rendering Method" (Metodo di rendering stereo) sia "Single Pass" o "Single Pass (Preview)" per PC e Android (selezionare l'icona del robot). Successivamente, compilare e caricare di nuovo e reimpostare Il mondo. 