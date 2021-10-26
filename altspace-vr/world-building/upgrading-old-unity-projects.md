---
title: Aggiornamento di progetti Unity vecchi
description: Informazioni su come aggiornare il contenuto alla versione più recente di Unity.
ms.date: 10/19/2021
ms.topic: article
keywords: kit, worlds, unity, aggiornamento, shader, caricatore, risoluzione dei problemi
ms.openlocfilehash: 06af70164e5bf870a10bf1ee9e949e09dfa69fd2
ms.sourcegitcommit: 8c58f9f9ad1a3f9534141dee2c78e32792d0db7a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2021
ms.locfileid: "130302415"
---
<a name="upgrading-old-unity-projects"></a>Aggiornamento di progetti Unity vecchi
=============================

Nel corso degli anni, AltspaceVR ha subito diversi aggiornamenti poco frequenti che richiedono agli utenti di modificare il contenuto. Se si verifica che un modello o un kit caricato in passato non è accessibile nella versione più recente di AltspaceVR, seguire questa guida per eseguire nuovamente il contenuto.

> [!NOTE]
> Prima di eseguire i passaggi descritti in questa guida, è consigliabile creare un backup completo del progetto nel caso in cui l'aggiornamento non venga eseguito senza problemi. Il modo più semplice è creare una seconda copia dell'intera cartella del progetto. Per una soluzione più avanzata, è consigliabile usare un sistema di controllo della versione come Git e GitHub.

<a name="overview"></a>Panoramica
---------

Al tempo della stesura di questo articolo, la versione corrente di AltspaceVR usa la configurazione seguente:

* Motore di gioco: Unity 2020.3.18f1 (accettabile anche: Unity 2020.3.9f1)
* Upload Strumento: Uploader 2.2
* Rendering: Universal Render Pipeline (URP)
* Modalità stereo: Single-Pass istanze (SPI) o Multiview on Quest

Se la versione del progetto Unity è precedente alla 2020.3, è probabile che sia necessario eseguire tutti questi aggiornamenti contemporaneamente, quindi seguire questa guida dall'inizio. Se si è già in Unity 2020.3, ma con Uploader 0.9, iniziare dal passaggio 6.

1. **ESEGUIRE IL BACKUP DEL PROGETTO:** creare una copia dell'intera directory del progetto e metterla in un luogo sicuro. Si tratta di un aggiornamento distruttivo, pertanto i file di progetto originali andranno persi dopo il completamento.
    Se si verificano problemi durante l'aggiornamento, sarà necessaria una copia pulita del progetto su cui eseguire il fall back.

2. **REMOVE OLD UPLOADER:** eseguire questo passaggio se il progetto usa AltspaceVR Uploader 0.8 o versioni precedenti. Con Unity chiuso, eliminare i file o le cartelle seguenti e i file con estensione meta corrispondenti. Se il file o la cartella non esiste, ignorarlo.

    * Asset/Altspace
    * Asset/plug-in
    * Assets/Prefabs/test-folder
    * Asset/prefab/Readme.txt
    * Assets/Resources/bg.jpeg
    * Assets/Resources/bg2.jpeg
    * Assets/Resources/logo.png
    * Assets/Resources/UserPreferences.asset
    * Assets/DFloor_v004.fbx

3. **REMOVE PROCESSED ASSETS (RIMUOVI ASSET ELABORATI)** - Eseguire questo passaggio se si esegue l'aggiornamento a una nuova versione di Unity. Con Unity chiuso, eliminare la cartella Library dal progetto. Si tratta di una cartella di sistema di Unity contenente gli asset e i file specifici del motore che vengono generati automaticamente dal contenuto della cartella Assets (tra le altre cose).

4. **SCARICA VERSIONE MOTORE:** eseguire questo passaggio se si esegue l'aggiornamento a una nuova versione di Unity. Aprire Unity Hub e installare Unity 2020.3.18f1 dall'archivio di download[(collegamento all'installazione del motore).](unityhub://2020.3.18f1/a7d1c678663c)
    * Se si compila in un PC Windows, selezionare le caselle per Android e Mac Build Support (Supporto build Android e Mac).
    * Se si compila in un Mac, selezionare le caselle android e Windows build.

5. **UPGRADE PROJECT** (AGGIORNA PROGETTO) - Aprire il progetto pulito in Unity 2020.3.18f1 e consentire a Unity di aggiornare il progetto.
    Questa operazione richiede tempo.

6. **SCARICARE IL CARICATORE:** scaricare la versione più recente di [Uploader](https://aka.ms/AvrUrpUploader)qui e salvarla nella cartella Packages del progetto. Questo file deve avere l'estensione ".tgz".
    > [!NOTE]
    > Se si usa il browser Safari per il download, verrà estratto automaticamente in un file "tar", che Unity non può usare. È possibile usare un browser diverso per il download oppure usare l'utilità di sistema "gzip" per comprimerlo nuovamente.
    
7. **INSTALL THE UPLOADER (INSTALLA** IL CARICATORE): installare il caricatore dalla gestione pacchetti dell'editor di Unity:
    1. Aprire la finestra di Gestione pacchetti Unity: Windows > Gestione pacchetti
    2. In alto a sinistra nella finestra fare clic sull'icona "+" e selezionare "Aggiungi pacchetto da tarball".
    3. Selezionare il file tgz scaricato nell'ultimo passaggio.
    4. Attendere che Unity disimballi il pacchetto.

8. **APRI IL CARICATORE:** se l'installazione ha avuto esito positivo, nella barra superiore sarà disponibile un menu "ALTSPACEVR".
    Questo menu contiene finestre separate per kit e modelli. Aprire quello più appropriato per il progetto.
    La prima volta che la finestra si apre, configurerà le impostazioni del progetto in modo che corrispondano al client del gioco Altspace: abilitazione della pipeline di rendering universale e Single-Pass istanze

9. **FIX SHADERS** : durante la prima esecuzione dell'installazione, è possibile che venga visualizzata temporaneamente una finestra di PowerShell.
    Potrebbe essere richiesto di aggiornare alcuni shader personalizzati/scaricati. Se si approva la richiesta, lo script di PowerShell tenterà di aggiornare automaticamente gli shader, ma le probabilità di esito positivo sono basse. È necessario controllare manualmente se lo shader funziona ancora correttamente in URP.

10. **FIX MATERIALS** (CORREGGI MATERIALI) - Alcuni o tutti i materiali possono diventare rosa/magenta durante il processo di aggiornamento. Indica un errore nello shader usato da tale materiale. Se sono stati usati gli shader predefiniti di Unity, in genere è possibile eseguirne automaticamente la migrazione a shader compatibili con URP dal menu: Edit > Render Pipeline > Universal Render Pipeline > Upgrade Project Materials to UniversalRP Materials (Modifica pipeline di rendering > universali > Upgrade Project Materials to UniversalRP Materials).

11. **COMPILAZIONE E CARICAMENTO:** a questo punto, il progetto dovrebbe essere completamente aggiornato. Seguire le istruzioni nella guida [Attività iniziali](world-building-toolkit-getting-started.md) per compilare e caricare il kit o il modello.

<a name="troubleshooting-tips"></a>Suggerimenti per la risoluzione dei problemi
---------------------

1. Se si scopre che il contenuto viene visualizzato solo con un occhio in modalità VR, è probabile che gli shader personalizzati in uso non supportino il rendering SPI. È necessario scegliere uno shader diverso o seguire la guida [all'aggiornamento SPI](https://docs.unity3d.com/Manual/SinglePassInstancing.html) di Unity per modificare manualmente lo shader e aggiungere il supporto.

2. Se si scopre che parte del contenuto è rosa/magenta nel gioco o è completamente invisibile, ciò può essere causato da uno shader incompatibile con URP. Sarà necessario sostituire lo shader o aggiornarlo manualmente.