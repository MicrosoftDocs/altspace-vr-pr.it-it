---
title: Guida di Unity Uploader
description: Rimanere aggiornati sulle domande frequenti più recenti e sulle soluzioni per AltspaceVR Unity Uploader.
ms.date: 02/10/2021
ms.topic: article
keywords: Guida, domande frequenti
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

Questa è la scena di Stargate Unity con un'app SDK che alimentato Gate e DND

**2. Sono un video learner, dove sono i miei video?**

[Guarda i video](https://youtu.be/km9CnVYPzoM)

**3. Dove è possibile trovare esempi?**

[Worlds in primo piano](https://account.altvr.com/worlds/featured) ed [esempi di Jimmy](https://account.altvr.com/worlds/1046572460192825569) sono buoni punti di partenza

**4. Funzionerà con Kit e il nuovo SDK?**
Sì, è possibile usare tutti gli strumenti insieme, se si desidera. Stiamo cercando di svilupparli per lavorare facilmente insieme.

**5. Supporta gli effetti delle particelle?**

![GIF degli effetti delle particelle di neve](images/uploader-faq-img-01.gif)

**6. È possibile ottenere l'audio spazializzato?**
Non al momento, ma è possibile inserire origini audio da riprodurre in aree localizzate. 

**7. L'illuminazione al forno funziona?**
Sì, ma le luci devono essere impostate su "baked" e non su "mixed"

**8. L'illuminazione globale funziona?**
Sì

**9. È sempre necessario reimpostare il mondo?**
Sì. È necessario ricaricare i bundle di asset unity ogni volta. 

**10. È possibile usare materiali e shader personalizzati?**

![GIF di materiali e shader personalizzati](images/uploader-faq-img-02.gif)

**11. È possibile caricare solo in una piattaforma?**
Sì, usando lo strumento Uploader. Tuttavia, le persone che sono in Android non vedono nulla nel mondo fino a quando non si carica la scena per la propria piattaforma. 

**12. Gli script sono consentiti?**
No, per motivi di sicurezza non è possibile consentire script o riferimenti a script. Se il caricamento contiene script o riferimenti a script, verrà rifiutato. Esaminare il nuovo SDK se è necessario creare script. 

**13. Quanto è grande una scena che è possibile caricare?**
È consigliabile iniziare da piccoli e tenere presenti gli utenti di Altspace che non hanno PC mostri. Detto questo, i giochi hanno portato le proprie mappe per i flussi live (ad esempio, Onward, a VR a vr arnesi)

![Screenshot del gioco VR in AltspaceVR](images/uploader-faq-img-03.png)

**14. È necessario ospitare i file di scena?**
No, Altspace sta servendo i file dopo averli caricati

**15. Le ombreggiature sono consentite?**
Sì

**16. Quanto velocemente è possibile eseguire l'iterazione usando uploader?**
Se si è già nel mondo, è possibile premere Upload in Uploader, reimpostare il mondo e visualizzare la scena aggiornata in appena 10 secondi. In genere, vengono visualizzati cicli da 30 secondi a pochi minuti a seconda della complessità della scena. Bevi un drink, te lo meriti di essere un World-Builder!

**17. Dove si ottengono i modelli 3D?**
Sketchfab, Sketchup, Minecraft, Unity Asset Store e così via.

**18. Supporta le animazioni?**

![GIF delle animazioni personalizzate in esecuzione](images/uploader-faq-img-04.gif)

**19. Come è possibile configurare l'audio spaziale?** Importare il file wav preferito, creare un oggetto gioco vuoto nella scena e selezionare questo oggetto. Trascinare e rilasciare il suono importato nel controllo dell'oggetto e verrà creata un'origine audio. Successivamente, regolare il volume su un valore non superiore a 0,5, impostare la fusione spaziale su 3D e regolare la distanza minima e massima per creare un'area audio appropriata. Viene visualizzato come sfera come collisori per impostazione predefinita. Per ottenere un vero drop off, è necessario regolare la curva di rilascio a proprio piacimento. [(tramite @IsThatToasted )](https://www.youtube.com/watch?v=ktb2vAAwknw&list=PLGmYIROty-5bpzKQNK3mRMi4pmh_LinV4&t=642s&index=29)

**20. Come mai vengono visualizzati gli occhi incrociati/le stranezze?**
In alcuni casi il caricatore non esegue correttamente l'override delle impostazioni di rendering. "Vai a Modifica > Project Impostazioni > Lettore". Assicurarsi che "XR Impostazioni > Virtual Reality Supported" sia selezionato e che "Stereo Rendering Method" sia "Single Pass" o "Single Pass (Preview)" per PC e Android (selezionare l'icona del robot). In seguito, compilare e caricare di nuovo e reimpostare il mondo. 