---
title: Guida dell'Uploader Unity
description: È possibile rimanere sempre aggiornati sulle domande e sulle soluzioni più recenti per l'Uploader Unity AltspaceVR.
ms.date: 02/10/2021
ms.topic: article
keywords: Guida, domande frequenti
ms.openlocfilehash: 814ff293cb98490900cd929f33477d15d3d668ae
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2021
ms.locfileid: "107213388"
---
# <a name="unity-uploader-help"></a>Guida dell'Uploader Unity

**1. quanto è impressionante questo strumento?**

> [!VIDEO https://channel9.msdn.com/Shows/Docs-Mixed-Reality/cheyenne-mountain-gate-room-v1/player]

Questa è la mia scena di Stargate Unity con un'app SDK che accende il controllo e DND

**2. sono uno Learner video, dove sono i miei video?**

[Guarda i nostri video](https://youtu.be/km9CnVYPzoM)

**3. dove è possibile trovare esempi?**

I [mondi disponibili](https://account.altvr.com/worlds/featured) e [gli esempi di Jimmy](https://account.altvr.com/worlds/1046572460192825569) sono ottimi punti di partenza

**4. funzionerà con i kit e il nuovo SDK?**
Sì, se si vuole, è possibile usare tutti gli strumenti insieme. Stiamo provando a svilupparle per collaborare in modo uniforme.

**5. supporta gli effetti particellari?**

![GIF degli effetti particellari neve](images/uploader-faq-img-01.gif)

**6. è possibile ottenere audio con spazialità?**
Non in questo momento, ma è possibile inserire le origini audio da riprodurre nelle aree localizzate. 

**7. l'illuminazione in forno funziona?**
Sì, ma le luci devono essere impostate su "baked" e non "mixed".

**8. l'illuminazione globale funziona?**
Sì

**9. è sempre necessario reimpostare il mondo?**
Sì. È necessario ricaricare ogni volta i bundle di asset di Unity. 

**10. è possibile usare i propri materiali e shader personalizzati?**

![GIF di materiali e shader personalizzati](images/uploader-faq-img-02.gif)

**11. è possibile caricare solo su una piattaforma?**
Sì, usando lo strumento Uploader. Tuttavia, le persone che si trovano in Android non vedranno nulla nel mondo fino a quando non si carica la scena per la piattaforma. 

**12. gli script sono consentiti?**
No, per motivi di sicurezza non è possibile consentire script o riferimenti a script. Se il caricamento contiene script o riferimenti a script, verrà rifiutato. Esaminare il nuovo SDK se il mondo necessita di script. 

**13. quali sono le dimensioni di una scena che è possibile caricare?**
Si consiglia di iniziare piccola e di tenere in considerazione le persone in Altspace che non hanno PC Monster. Ciò premesso, abbiamo giochi che portano le mappe per i flussi live, ad esempio, in seguito, un gioco sparatutto VR

![Screenshot del gioco VR in AltspaceVR](images/uploader-faq-img-03.png)

**14. è necessario ospitare i file della scena?**
No, Altspace sta servendo i file una volta caricati

**15. le ombreggiature sono consentite?**
Sì

**16. quanto velocemente è possibile eseguire l'iterazione usando l'Uploader?**
Se ci si trova già nel mondo, è possibile premere carica nell'Uploader, reimpostare il mondo e visualizzare la scena aggiornata in un minimo di 10 secondi. In genere, i cicli verranno visualizzati da 30 secondi a pochi minuti, a seconda della complessità della scena. È possibile bere, perché si merita di essere un mondo di costruttori.

**17. dove si ottengono I modelli 3D?**
Sketchfab, SketchUp, Minecraft, Unity Asset Store e così via.

**18. supporta le animazioni?**

![GIF di animazioni personalizzate in esecuzione](images/uploader-faq-img-04.gif)

**19. come è possibile configurare l'audio spaziale?** Importare il file wav desiderato, creare un oggetto gioco vuoto nella scena e selezionare questo oggetto. Trascinare e rilasciare il suono importato nel controllo dell'oggetto e creerà un'origine audio. Modificare quindi il volume in modo che non superi 0,5, modificare la combinazione spaziale in 3D e modificare la distanza minima e massima per creare un'area corretta del suono. Per impostazione predefinita, questo valore viene visualizzato come Sphere come Collider. Per ottenere una vera e propria riduzione, è necessario modificare la curva di riduzione a piacimento. [(tramite @IsThatToasted )](https://www.youtube.com/watch?v=ktb2vAAwknw&list=PLGmYIROty-5bpzKQNK3mRMi4pmh_LinV4&t=642s&index=29)

**20. come vengono visualizzati gli occhi incrociati/bizzarri?**
Talvolta il caricatore non sostituisce correttamente le impostazioni di rendering. "Vai a modifica > impostazioni progetto > lettore". Verificare che siano selezionate le impostazioni "XR > Virtual Reality supported" e che "metodo di rendering stereo" sia "single pass" o "single pass (Preview)" per PC e Android (selezionare l'icona del robot). Successivamente, compilare e caricare nuovamente e reimpostare il mondo. 