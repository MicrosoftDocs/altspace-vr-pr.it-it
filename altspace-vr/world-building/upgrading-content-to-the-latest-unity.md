---
title: Aggiornamento del contenuto alla versione più recente di Unity
description: Informazioni su come aggiornare il contenuto alla versione più recente di Unity.
ms.date: 06/4/2021
ms.topic: article
keywords: kit, mondi, unity, aggiornamento, shader, caricatore, risoluzione dei problemi
ms.openlocfilehash: a10e64b4dc19e256dcae9d61620de0140db60ccc0bf2a10dc864313f139bbd10
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126762"
---
# <a name="updating-content-to-the-latest-unity-version"></a>Aggiornamento del contenuto alla versione più recente di Unity

## <a name="moving-to-unity-202039"></a>Passaggio a Unity 2020.3.9

A partire da oggi, AltspaceVR è stato aggiornato a una versione recente di Unity (2020.3.9). Oltre ad alcuni miglioramenti delle prestazioni, questo aggiornamento offre funzionalità future che non vediamo l'ora di incorporare. Questa modifica deve essere compatibile con tutto il contenuto esistente. In caso contrario, è possibile contattare il supporto tecnico: altvr.com/support

Anche se questo passaggio alla versione 2020.3.9 non ha interessato il contenuto generato dall'utente, in poche settimane verrà apportata una modifica alla modalità [di rendering stereo]( https://docs.unity3d.com/Manual/SinglePassStereoRendering.html)di AltspaceVR che richiederà agli utenti di aggiornare il contenuto. Questo aggiornamento a [Single Pass Instancing](https://docs.unity3d.com/Manual/SinglePassInstancing.html) consentirà miglioramenti significativi delle prestazioni nel mondo. Tenere presente che questa nuova build non supporterà più la compatibilità con le versioni precedenti con il contenuto della versione 2019.4 e versioni precedenti. È urgente che tutto il contenuto di proprietà dell'autore sia aggiornato appena possibile per evitare modifiche di rilievo. Seguire la guida seguente per aggiornare il contenuto e garantire una transizione graduale all'istanza a passaggio singolo in Unity 2020.3.9.

> [!NOTE]
> Se si usano regolarmente contenuti di proprietà di un altro utente che sono stati condivisi con l'utente, contattare il proprietario del kit/mondo e assicurarsi che abbia intenzione di aggiornarne il contenuto.

> Se si è un autore di contenuti e si hanno domande o si richiede assistenza, contattare il team di supporto per assistenza: altvr.com/support

## <a name="testing-your-spi-content"></a>Test del contenuto SPI

Usare le versioni di anteprima seguenti di AltspaceVR per testare il contenuto appena aggiornato in VR. Le versioni di anteprima sono solo a scopo di test e non devono essere usate per un uso generale della piattaforma.

* [AltspaceVR SPI Preview per Windows Mixed Reality](https://aka.ms/AvrSpiMr)
* [AltspaceVR SPI Preview for SteamVR](https://aka.ms/AvrSpiSteam)
* [AltspaceVR SPI Preview for Oculus Rift](https://aka.ms/AvrSpiRift)

> Nota: sono state fornite solo le anteprime di PC VR. Il rendering con istanza a passaggio singolo non è disponibile in Android e non è necessario in piattaforme non VR come Mac. È quindi possibile usare la versione di versione generale per testare questi dispositivi.


## <a name="storecompatibilitycheck"></a>Controllo di compatibilità dell'archivio

L'aggiornamento a Unity 2020.3.9 influirà anche sulla compatibilità visore e store-build. È ora necessario scaricare AltspaceVR dallo store compatibile con il visore. Ad esempio: per un visore WinMR o Oculus, scaricare altspaceVR rispettivamente da Windows Store o Oculus Store. Windows Mixed Reality utenti devono scaricare AltspaceVR da Windows Store, gli utenti di SteamVR da Steam e oculus Rift da Oculus Store.

## <a name="altspacevr-uploader-v090-upgrade-guide"></a>Guida all'aggiornamento di AltspaceVR Uploader v0.9.0 

Uploader 0.9 è in pacchetto in modo diverso rispetto alle versioni precedenti di Uploader. Contemporaneamente a questa modifica di creazione pacchetti, il nuovo caricatore richiede una nuova versione di Unity. Questa guida ha lo scopo di rendere questo processo di aggiornamento più semplice e sicuro per tutti gli interessati.

1. **ESEGUIRE IL BACKUP DEL PROGETTO:** creare una copia dell'intera directory del progetto e metterla al sicuro. Questo aggiornamento è un aggiornamento distruttivo, quindi non sarà possibile creare o caricare bundle per Unity 2019.4 dopo il completamento. Se si verificano problemi durante questo aggiornamento, sarà necessaria una copia pulita del progetto su cui eseguire il fall back. Sarà anche necessario per aggiornare i kit o i modelli live prima che AltspaceVR eserviti ufficialmente l'aggiornamento a Unity 2020.3.9.

2. **REMOVE OLD UPLOADER** : con Unity chiuso, eliminare i file/cartelle seguenti e i file con estensione meta corrispondenti:

    ```console
    * Assets/Altspace

    * Assets/Plugins

    * Assets/Prefabs/test-folder, Readme.txt

    * Assets/Resources/bg.jpeg, bg2.jpeg, logo.png, UserPreferences.asset

    * Assets/DFloor_v004.fbx

    * Library (This is a Unity system folder, not an Uploader folder. Delete it anyway, and let it be rebuilt during the upgrade.)
    ```

3. **DOWNLOAD ENGINE VERSION** (SCARICA VERSIONE MOTORE): aprire Unity Hub e installare Unity 2020.3.9 (oppure fare clic [qui](https://unity3d.com/ru/unity/whats-new/2020.3.9) per eseguire l'installazione diretta).

4. **UPGRADE PROJECT** : aprire il progetto pulito in Unity 2020.3.9 e consentire a Unity di aggiornare il progetto.

5. (Solo PC) **DOWNLOAD MIXED REALITY FEATURE TOOL** : seguire le istruzioni per scaricare lo strumento [di](/windows/mixed-reality/develop/unity/welcome-to-mr-feature-tool)funzionalità di realtà mista, che verrà utilizzato per gestire l'installazione del pacchetto uploader.

6. **INSTALLARE IL CARICATORE** : usare mr feature tool per selezionare il progetto Unity e aggiungere la funzionalità AltspaceVR Uploader (sotto l'intestazione AltspaceVR). Seguire le istruzioni nello strumento.

In macOS scaricare manualmente la [](https://dev.azure.com/aipmr/MixedReality-Unity-Packages/_packaging?_a=package&feed=Unity-packages&package=com.microsoft.altspacevr_uploader&protocolType=Npm&version=0.9.0&view=versions)versione più recente dal Registro di sistema e installarla da Gestione pacchetti dell'editor di Unity (Windows > Gestione pacchetti > + > Aggiungi pacchetto da tarball).

Al termine dell'importazione del pacchetto, la finestra del caricatore familiare dovrebbe essere disponibile nella voce di menu AltspaceVR.

## <a name="troubleshooting-tips"></a>Suggerimenti per la risoluzione dei problemi

1. Se si verificano problemi di controller o input sul visore WinMR, assicurarsi che sia posizionato sulla testa per attivare correttamente il sensore di presenza. Si tratta di un problema noto e Microsoft sta lavorando attivamente per risolverlo.

2. Controllare il visore e la compatibilità store-build. Se si usa un visore WinMR, ad esempio, assicurarsi che la build altspaceVR sia stata acquisita tramite il Windows Store.

3. Se durante i test si scopre che il contenuto viene visualizzato solo in un occhio in modalità VR, è probabile che gli shader personalizzati in uso non supportino il rendering SPI. È necessario scegliere uno shader diverso o seguire la guida [all'aggiornamento SPI](https://docs.unity3d.com/Manual/SinglePassInstancing.html) di Unity per modificare manualmente lo shader e aggiungere il supporto.

4. Per quelli in WinMR, tenere presente che prima di poter accedere alla modalità VR in AltspaceVR, è necessario: 
    1. Scaricare e installare OpenXR per Windows Mixed Reality dal Microsoft Store.
        1. Aprire l'app Portale realtà mista app
        2. Nell'angolo inferiore sinistro dell'app selezionare "Altro"
        3. Nel menu visualizzato selezionare Configura OpenXR. In questo modo verrà avviato Windows Store da cui è possibile installare il runtime. Se questa voce di menu non viene visualizzata, OpenXR potrebbe essere già installato nel PC.