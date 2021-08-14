---
title: Aggiornamento del contenuto alla versione più recente di Unity
description: Informazioni su come aggiornare il contenuto alla versione più recente di Unity.
ms.date: 06/4/2021
ms.topic: article
keywords: kit, worlds, unity, aggiornamento, shader, caricatore, risoluzione dei problemi
ms.openlocfilehash: a10e64b4dc19e256dcae9d61620de0140db60ccc0bf2a10dc864313f139bbd10
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126762"
---
# <a name="updating-content-to-the-latest-unity-version"></a>Aggiornamento del contenuto alla versione più recente di Unity

## <a name="moving-to-unity-202039"></a>Passaggio a Unity 2020.3.9

A partire da oggi, AltspaceVR è stato aggiornato a una versione recente di Unity (2020.3.9). Oltre ad alcuni miglioramenti delle prestazioni, questo aggiornamento rappresenta una prova per le prossime funzionalità che microsoft è contenta di incorporare. Questa modifica deve essere compatibile con tutto il contenuto esistente. In caso contrario, contattare il supporto tecnico: altvr.com/support

Anche se questo passaggio alla versione 2020.3.9 non ha inciso sul contenuto generato dall'utente, in alcune settimane verrà apportata una modifica alla modalità [di rendering stereo]( https://docs.unity3d.com/Manual/SinglePassStereoRendering.html)di AltspaceVR che richiederà agli utenti di aggiornare il contenuto . Questo aggiornamento alla [funzionalità single pass-instancing](https://docs.unity3d.com/Manual/SinglePassInstancing.html) consentirà di migliorare notevolmente le prestazioni in tutto il mondo. Tenere presente che questa nuova build non supporterà più la compatibilità con le versioni precedenti con il contenuto della versione 2019.4 e precedenti. È urgente che tutto il contenuto di proprietà dell'autore sia aggiornato appena possibile per evitare modifiche di rilievo. Seguire la guida seguente per aggiornare il contenuto e garantire una transizione senza problemi a Single Pass Instancing in Unity 2020.3.9.

> [!NOTE]
> Se si usa regolarmente contenuto di proprietà di un altro utente che è stato condiviso con l'utente, contattare il proprietario del kit/mondo e assicurarsi che abbia in programma di aggiornare il contenuto.

> Se si è un autore di contenuti e si hanno domande o si richiede assistenza, contattare il team di supporto per assistenza: altvr.com/support

## <a name="testing-your-spi-content"></a>Test del contenuto SPI

Usare le versioni di anteprima seguenti di AltspaceVR per testare il contenuto appena aggiornato nella realtà virtuale. Le versioni di anteprima sono solo a scopo di test e non devono essere usate per un uso generale della piattaforma.

* [AltspaceVR SPI Preview for Windows Mixed Reality](https://aka.ms/AvrSpiMr)
* [AltspaceVR SPI Preview for SteamVR](https://aka.ms/AvrSpiSteam)
* [AltspaceVR SPI Preview for Oculus Rift](https://aka.ms/AvrSpiRift)

> Nota: sono state fornite solo le anteprime della realtà virtuale per PC. Il rendering con istanze a singolo passaggio non è disponibile in Android e non è necessario in piattaforme non VR come Mac. È quindi possibile usare la versione di rilascio generale per testare questi dispositivi.


## <a name="storecompatibilitycheck"></a>Controllo di compatibilità dell'archivio

L'aggiornamento a Unity 2020.3.9 influirà anche sulla compatibilità del visore VR e della build dello store. È ora necessario scaricare AltspaceVR dallo Store compatibile con il visore VR. Ad esempio: per un visore VR WinMR o Oculus, scaricare altspaceVR rispettivamente da Windows Store o Oculus Store. Windows Mixed Reality gli utenti devono scaricare AltspaceVR da Windows Store, gli utenti di SteamVR da Steam e gli utenti di Oculus Rift da Oculus Store.

## <a name="altspacevr-uploader-v090-upgrade-guide"></a>Guida all'aggiornamento di AltspaceVR Uploader v0.9.0 

Uploader 0.9 è in pacchetto in modo diverso rispetto alle versioni precedenti di Uploader. Contemporaneamente a questa modifica del pacchetto, il nuovo caricatore richiede una nuova versione di Unity. Questa guida ha lo scopo di rendere questo processo di aggiornamento più semplice e sicuro per tutti gli utenti coinvolti.

1. **ESEGUIRE IL BACKUP DEL PROGETTO:** creare una copia dell'intera directory del progetto e metterla in un luogo sicuro. Questo aggiornamento è distruttivo, quindi non sarà possibile creare o caricare bundle per Unity 2019.4 dopo il completamento. Se si verificano problemi durante l'aggiornamento, sarà necessaria una copia pulita del progetto su cui eseguire il fall back. Sarà necessario anche per aggiornare i kit live o i modelli prima dell'aggiornamento ufficiale di AltspaceVR a Unity 2020.3.9.

2. **REMOVE OLD UPLOADER** : con Unity chiuso, eliminare i file/cartelle seguenti e i file con estensione meta corrispondenti:

    ```console
    * Assets/Altspace

    * Assets/Plugins

    * Assets/Prefabs/test-folder, Readme.txt

    * Assets/Resources/bg.jpeg, bg2.jpeg, logo.png, UserPreferences.asset

    * Assets/DFloor_v004.fbx

    * Library (This is a Unity system folder, not an Uploader folder. Delete it anyway, and let it be rebuilt during the upgrade.)
    ```

3. **SCARICARE LA VERSIONE DEL** MOTORE: aprire Unity Hub e installare Unity 2020.3.9 (oppure fare clic [qui](https://unity3d.com/ru/unity/whats-new/2020.3.9) per eseguire direttamente l'installazione).

4. **UPGRADE PROJECT** (AGGIORNA PROGETTO) - Aprire il progetto pulito in Unity 2020.3.9 e consentire a Unity di aggiornare il progetto.

5. (Solo PC) **DOWNLOAD MIXED REALITY FEATURE TOOL (SCARICA** STRUMENTO PER LE FUNZIONALITÀ DI REALTÀ MISTA) - Seguire le istruzioni per scaricare [Mixed Reality Feature Tool,](/windows/mixed-reality/develop/unity/welcome-to-mr-feature-tool)che verrà utilizzato per gestire l'installazione del pacchetto di Uploader.

6. **INSTALLARE IL CARICATORE:** usare MR Feature Tool per selezionare il progetto Unity e aggiungere la funzionalità AltspaceVR Uploader (sotto l'intestazione AltspaceVR). Seguire le istruzioni nello strumento.

In macOS scaricare manualmente la [](https://dev.azure.com/aipmr/MixedReality-Unity-Packages/_packaging?_a=package&feed=Unity-packages&package=com.microsoft.altspacevr_uploader&protocolType=Npm&version=0.9.0&view=versions)versione più recente dal Registro di sistema e installarla dalla gestione pacchetti dell'editor unity (Windows > Gestione pacchetti > + > Aggiungi pacchetto da tarball).

Al termine dell'importazione del pacchetto, la familiare finestra uploader dovrebbe essere disponibile nella voce di menu ALTSPACEVR.

## <a name="troubleshooting-tips"></a>Suggerimenti per la risoluzione dei problemi

1. Se si verificano problemi di controller o di input sul visore VR WinMR, assicurarsi che sia posizionato sulla testa per coinvolgere correttamente il sensore di presenza. Si tratta di un problema noto e Microsoft sta lavorando attivamente per risolverlo.

2. Controllare il visore VR e la compatibilità della compilazione dello store. Se ad esempio si usa un visore VR WinMR, assicurarsi che la build di AltspaceVR sia stata acquisita tramite Windows Store.

3. Se durante i test si scopre che il contenuto viene visualizzato solo in modalità VR, è probabile che gli shader personalizzati in uso non supportino il rendering SPI. È necessario scegliere uno shader diverso o seguire la guida [all'aggiornamento SPI](https://docs.unity3d.com/Manual/SinglePassInstancing.html) di Unity per modificare manualmente lo shader e aggiungere il supporto.

4. Per quelli in WinMR, tenere presente che prima di poter accedere alla modalità VR in AltspaceVR, è necessario: 
    1. Scaricare e installare OpenXR per Windows Mixed Reality dalla Microsoft Store.
        1. Aprire l'app Portale realtà mista app
        2. Nell'angolo inferiore sinistro dell'app selezionare "Vedi altro"
        3. Nel menu visualizzato selezionare Configura OpenXR. Questa operazione causerà l'avvio Windows Store da cui è possibile installare il runtime. Se questa voce di menu non viene visualizzata, OpenXR potrebbe essere già installato nel PC.