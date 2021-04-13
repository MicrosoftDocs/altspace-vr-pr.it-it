---
title: Uso della console multimediale
description: Informazioni su come iniziare a configurare, pubblicare e controllare la console multimediale nelle esperienze di AltspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: Console, Multimedia
ms.openlocfilehash: 601328eb6f266dbcfc9d81fc4f1c2d09ac62b318
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2021
ms.locfileid: "107212840"
---
# <a name="using-the-multimedia-console"></a><span data-ttu-id="6de77-104">Uso della console multimediale</span><span class="sxs-lookup"><span data-stu-id="6de77-104">Using the multimedia console</span></span>

<span data-ttu-id="6de77-105">La console multimediale è uno strumento che consente la condivisione di contenuti multimediali in eventi e mondi.</span><span class="sxs-lookup"><span data-stu-id="6de77-105">The Multimedia Console is a tool that enables media sharing in events and worlds.</span></span> <span data-ttu-id="6de77-106">È possibile usarlo per condividere elementi quali immagini, diapositive di presentazione, Livestream, video, playlist e altro ancora.</span><span class="sxs-lookup"><span data-stu-id="6de77-106">You can use it to share things like images, presentation slides, livestreams, videos, playlists, and more.</span></span> <span data-ttu-id="6de77-107">Di seguito sono riportate istruzioni dettagliate su come usare la console multimediale **v 0.5.0 +**.</span><span class="sxs-lookup"><span data-stu-id="6de77-107">Below is a step-by-step instruction on how to use the Multimedia Console **v0.5.0+**.</span></span> 

## <a name="getting-started"></a><span data-ttu-id="6de77-108">Introduzione</span><span class="sxs-lookup"><span data-stu-id="6de77-108">Getting started</span></span>

<span data-ttu-id="6de77-109">La Guida introduttiva alla console multimediale è un processo in due parti.</span><span class="sxs-lookup"><span data-stu-id="6de77-109">Getting started with the Multimedia Console is a two part process.</span></span>  <span data-ttu-id="6de77-110">Per prima cosa, è disponibile il portale Web che verrà usato per generare e pubblicare una configurazione per la sessione della console multimediale che viene posizionata nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="6de77-110">First there's the web portal that you'll use to generate and publish a configuration for the Multimedia Console session you place in your environment.</span></span>  <span data-ttu-id="6de77-111">Il secondo è la posizione dell'app console multimediale effettiva nell'ambiente e l'impostazione del codice di configurazione da usare.</span><span class="sxs-lookup"><span data-stu-id="6de77-111">Second is the placement of the actual Multimedia Console app in your environment and setting the configuration code it should use.</span></span>

### <a name="configuring-the-multimedia-console-with-the-web-portal"></a><span data-ttu-id="6de77-112">Configurazione della console multimediale con il portale Web</span><span class="sxs-lookup"><span data-stu-id="6de77-112">Configuring the Multimedia console with the web portal</span></span>

1. <span data-ttu-id="6de77-113">Prima di tutto, è necessario assicurarsi che il contenuto sia ospitato online perché è necessario un URL.</span><span class="sxs-lookup"><span data-stu-id="6de77-113">First, you'll need to make sure your content is hosted online because you'll need a URL.</span></span> <span data-ttu-id="6de77-114">(È possibile caricare le foto in altvr.com, ospitare un file video. MP4 in linea o usare il collegamento di streaming live: https://www.twitch.tv/ninja)</span><span class="sxs-lookup"><span data-stu-id="6de77-114">(You can upload photos to altvr.com, host a video .mp4 file online or use Twitch live stream link: https://www.twitch.tv/ninja)</span></span> 
2. <span data-ttu-id="6de77-115">Passare al portale Web per la console multimediale all'indirizzo [https://multimedia-console.altvr.com/](https://multimedia-console.altvr.com/)</span><span class="sxs-lookup"><span data-stu-id="6de77-115">Navigate to the web portal for the Multimedia Console at [https://multimedia-console.altvr.com/](https://multimedia-console.altvr.com/)</span></span>
3. <span data-ttu-id="6de77-116">Dal portale Web è possibile generare e pubblicare una configurazione per la console multimediale.</span><span class="sxs-lookup"><span data-stu-id="6de77-116">From the web portal, you can generate and publish a configuration for the Multimedia Console.</span></span>  <span data-ttu-id="6de77-117">(Vedere di seguito per informazioni dettagliate sulle varie proprietà).</span><span class="sxs-lookup"><span data-stu-id="6de77-117">(See below for details about the various properties).</span></span>
4. <span data-ttu-id="6de77-118">Dopo aver immesso il supporto nell'elenco dei supporti e aver configurato le impostazioni generali, selezionare il pulsante pubblica nella parte superiore destra dell'app.</span><span class="sxs-lookup"><span data-stu-id="6de77-118">Once you've entered the media into the media list and have configured the general settings, select the publish button in the top-right part of the app.</span></span>
5. <span data-ttu-id="6de77-119">Una volta completata la pubblicazione, viene visualizzata una finestra di dialogo con un codice di due parole per poter accedere alla console multimediale inserita.</span><span class="sxs-lookup"><span data-stu-id="6de77-119">Once the publish has completed, a dialog will pop up with a two word code for you to enter in to the Multimedia Console you placed.</span></span>
  
### <a name="placing-the-multimedia-console-in-your-environment"></a><span data-ttu-id="6de77-120">Inserimento della console multimediale nell'ambiente</span><span class="sxs-lookup"><span data-stu-id="6de77-120">Placing the Multimedia console in your environment</span></span>

1. <span data-ttu-id="6de77-121">Selezionare nel **Pannello editor > editor del mondo > App SDK > console multimediale**.</span><span class="sxs-lookup"><span data-stu-id="6de77-121">Select on **World Editor > Editor Panel > SDK Apps > Multimedia Console**.</span></span> <span data-ttu-id="6de77-122">Non passare all' **editor globale > nozioni di base > App SDK**, ovvero per le app non registrate.</span><span class="sxs-lookup"><span data-stu-id="6de77-122">(Don't go to **World Editor > Basics > SDK App**--that's for unregistered apps.)</span></span>  
2. <span data-ttu-id="6de77-123">Posizionare la console multimediale per la migliore suite di spazio e destinatari.</span><span class="sxs-lookup"><span data-stu-id="6de77-123">Position the Multimedia Console to best suite your space and audience.</span></span>
3. <span data-ttu-id="6de77-124">Per uscire dalla modalità di modifica, fare clic sul pulsante arancione della modalità di modifica.</span><span class="sxs-lookup"><span data-stu-id="6de77-124">Get out of Edit Mode by clicking the orange Edit Mode button.</span></span>
4. <span data-ttu-id="6de77-125">Verrà richiesto di immettere **il proprietario del Media Player?**</span><span class="sxs-lookup"><span data-stu-id="6de77-125">You'll be prompted **Are you the media player owner?**</span></span> <span data-ttu-id="6de77-126">Se si è l'utente che deve essere il proprietario ufficiale della sessione della console multimediale, confermare e continuare.</span><span class="sxs-lookup"><span data-stu-id="6de77-126">If you're the person who should be the official owner of this Multimedia Console session, confirm and continue.</span></span> <span data-ttu-id="6de77-127">Sono disponibili anche altri ruoli con autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="6de77-127">(Other permissioned roles are available as well.</span></span> <span data-ttu-id="6de77-128">Per un elenco dettagliato, vedere di seguito.</span><span class="sxs-lookup"><span data-stu-id="6de77-128">See below for a detailed list.)</span></span>
5. <span data-ttu-id="6de77-129">Selezionare Sì per confermare che si è l'host primario.</span><span class="sxs-lookup"><span data-stu-id="6de77-129">Select Yes to confirm that you are the primary host.</span></span>  
6. <span data-ttu-id="6de77-130">Verrà visualizzata una finestra di dialogo che richiede di immettere un codice dal portale Web o da JSON valido.</span><span class="sxs-lookup"><span data-stu-id="6de77-130">A dialog should pop up that asks you to enter a code from the web portal or valid JSON.</span></span>  <span data-ttu-id="6de77-131">Immettere il codice di due parole dal portale Web, incluso il trattino, e fare clic su OK.</span><span class="sxs-lookup"><span data-stu-id="6de77-131">Enter the two word code from the web portal including the dash and hit OK.</span></span> <span data-ttu-id="6de77-132">(JSON è una configurazione avanzata descritta di seguito)</span><span class="sxs-lookup"><span data-stu-id="6de77-132">(JSON is an advanced configuration described below)</span></span>
7. <span data-ttu-id="6de77-133">La console multimediale dovrebbe essere caricata dopo alcuni secondi con la configurazione creata nel portale Web.</span><span class="sxs-lookup"><span data-stu-id="6de77-133">The Multimedia Console should load after a few seconds with the configuration you built in the web portal.</span></span>

### <a name="controlling-the-multimedia-console"></a><span data-ttu-id="6de77-134">Controllo della console multimediale</span><span class="sxs-lookup"><span data-stu-id="6de77-134">Controlling the Multimedia console</span></span>

1. <span data-ttu-id="6de77-135">Dopo aver inserito il codice e completato il processo di configurazione, verranno visualizzati i pulsanti di controllo sotto uno schermo multimediale.</span><span class="sxs-lookup"><span data-stu-id="6de77-135">After you input your code and complete the configuration process, you'll see control buttons appear below a media display.</span></span> 
    * <span data-ttu-id="6de77-136">**Play** avvia il Visualizzatore multimediale (o riavvia in corrispondenza della voce corrente, se in precedenza è stato arrestato)</span><span class="sxs-lookup"><span data-stu-id="6de77-136">**Play** starts the media viewer (or restarts at current entry, if previously stopped)</span></span> 
    * <span data-ttu-id="6de77-137">**Stop** arresta il Visualizzatore multimediale e nasconde i supporti correnti.</span><span class="sxs-lookup"><span data-stu-id="6de77-137">**Stop** stops the media viewer, and hides current media.</span></span>  
    * <span data-ttu-id="6de77-138">**Avanti/indietro** ignora i supporti successivi o precedenti</span><span class="sxs-lookup"><span data-stu-id="6de77-138">**Next/Prev** skips to next or previous media</span></span> 
    * <span data-ttu-id="6de77-139">**x/x**   Mostra l'indice corrente nell'elenco dei supporti e consente di passare a un punto qualsiasi dell'elenco</span><span class="sxs-lookup"><span data-stu-id="6de77-139">**x/x** shows the current index into the media list, and allows you to jump to any point in the list</span></span>
    * <span data-ttu-id="6de77-140">**Config** consente di reimmettere un nuovo codice dal portale Web per impostare una nuova configurazione nella console di.</span><span class="sxs-lookup"><span data-stu-id="6de77-140">**Config** allows reentering a new code from the web portal to set a new configuration in the console.</span></span> 

<span data-ttu-id="6de77-141">A questo punto è possibile iniziare la condivisione tramite la console multimediale.</span><span class="sxs-lookup"><span data-stu-id="6de77-141">Now you're set to begin sharing via the Multimedia Console!</span></span>  
 
## <a name="working-with-the-web-portal"></a><span data-ttu-id="6de77-142">Uso del portale Web</span><span class="sxs-lookup"><span data-stu-id="6de77-142">Working with the web portal</span></span>

<span data-ttu-id="6de77-143">Il portale Web è un'app Web che consente di configurare le varie funzionalità della console multimediale.</span><span class="sxs-lookup"><span data-stu-id="6de77-143">The web portal is a web app that enables configuring the various features of the Multimedia Console.</span></span>  <span data-ttu-id="6de77-144">Queste funzionalità rientrino in due categorie: impostazioni generali della console multimediale e Media Play List.</span><span class="sxs-lookup"><span data-stu-id="6de77-144">These features fall in to two categories; general media console settings, and the media play list.</span></span>

### <a name="multimedia-console-general-settings"></a><span data-ttu-id="6de77-145">Impostazioni generali della console multimediale</span><span class="sxs-lookup"><span data-stu-id="6de77-145">Multimedia console general settings</span></span>

<span data-ttu-id="6de77-146">**Impostazioni di riproduzione**</span><span class="sxs-lookup"><span data-stu-id="6de77-146">**Playback Settings**</span></span>

<span data-ttu-id="6de77-147">Impostazioni di riproduzione generale per l'elenco dei supporti</span><span class="sxs-lookup"><span data-stu-id="6de77-147">General playback settings for the media list</span></span>

* <span data-ttu-id="6de77-148">**Elenco supporti ciclo**: determina se l'elenco dei supporti deve essere in loop una volta raggiunta la fine dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="6de77-148">**Loop Media List**- Determines whether the media list should loop around once you reach the end of the list.</span></span>
* <span data-ttu-id="6de77-149">**Metodo Start** : seleziona il metodo in base al quale deve essere avviata la console multimediale.</span><span class="sxs-lookup"><span data-stu-id="6de77-149">**Start Method** - Selects the method by which the multimedia console should start.</span></span>
    * <span data-ttu-id="6de77-150">Manual: attende che venga premuto il pulsante Play prima di avviare il supporto</span><span class="sxs-lookup"><span data-stu-id="6de77-150">Manual - Waits for the play button to be pressed before starting the media</span></span>
    * <span data-ttu-id="6de77-151">Avvio automatico dall'inizio-avvio automatico dell'elenco dei supporti dall'inizio dell'elenco</span><span class="sxs-lookup"><span data-stu-id="6de77-151">Auto Start from Beginning - Auto start the media list from the beginning of the list</span></span>
    * <span data-ttu-id="6de77-152">Avvio automatico casuale: avvia automaticamente il supporto da un punto di partenza casuale nell'elenco</span><span class="sxs-lookup"><span data-stu-id="6de77-152">Auto Start Random - Auto starts the media from a random starting point in the list</span></span>

<span data-ttu-id="6de77-153">**Ruoli**</span><span class="sxs-lookup"><span data-stu-id="6de77-153">**Roles**</span></span>

<span data-ttu-id="6de77-154">Assegnazioni di ruolo per il controllo e la configurazione della console multimediale.</span><span class="sxs-lookup"><span data-stu-id="6de77-154">Role assignments for controlling and configuring the Multimedia Console.</span></span>    <span data-ttu-id="6de77-155">Questi ruoli sono suddivisi nel seguente set:</span><span class="sxs-lookup"><span data-stu-id="6de77-155">These roles are broken down in to the following set:</span></span>

* <span data-ttu-id="6de77-156">**Solo proprietario** : l'utente proprietario della sessione della console multimediale</span><span class="sxs-lookup"><span data-stu-id="6de77-156">**Owner Only** - The user that is the owner of the Multimedia Console Session</span></span>
* <span data-ttu-id="6de77-157">**Utenti con privilegi elevati** : utenti con ruoli di moderatore, host o Presenter nello spazio in cui la console multimediale è configurata originariamente</span><span class="sxs-lookup"><span data-stu-id="6de77-157">**Elevated Users** - Users that have moderator, host, or presenter roles in the space that the Multimedia Console is configured in originally</span></span>
* <span data-ttu-id="6de77-158">**Tutti gli utenti** -tutti gli utenti</span><span class="sxs-lookup"><span data-stu-id="6de77-158">**All Users** - All users</span></span>

<span data-ttu-id="6de77-159">Questo stack di ruoli nel senso che a tutti i ruoli sopra a quello scelto in questo elenco verrà inoltre concessa l'autorizzazione per l'utilizzo di tale funzionalità.</span><span class="sxs-lookup"><span data-stu-id="6de77-159">These roles stack in the sense that all roles above the one chosen in this list will also be granted permission to use that feature.</span></span>  <span data-ttu-id="6de77-160">Esempio: **gli utenti con privilegi elevati** includono il **proprietario** anche se non sono un moderatore, un host o un presentatore \* \* in AltspaceVR.</span><span class="sxs-lookup"><span data-stu-id="6de77-160">Example: **Elevated Users** includes the **Owner** even if they aren't a moderator, host, or presenter\*\* in AltspaceVR.</span></span> <span data-ttu-id="6de77-161">Di seguito sono riportate le funzionalità controllate dalle assegnazioni di ruolo</span><span class="sxs-lookup"><span data-stu-id="6de77-161">Features that are controlled by role assignments are as follows</span></span>

* <span data-ttu-id="6de77-162">**Consente di controllare il lettore multimediale** : determina quali ruoli possono controllare i pulsanti di riproduzione dei supporti per la console multimediale</span><span class="sxs-lookup"><span data-stu-id="6de77-162">**Can control media player** - Determines what roles can control the media playback buttons for the Multimedia Console</span></span>
* <span data-ttu-id="6de77-163">**Può configurare Media Player** : determina i ruoli che possono configurare la console multimediale, a cui viene concesso l'accesso al pulsante **config**</span><span class="sxs-lookup"><span data-stu-id="6de77-163">**Can configure the media player** - Determines what roles can configure the Multimedia Console by being granted access to the **Config** button</span></span>

### <a name="adding-photos-and-videos-to-the-media-list"></a><span data-ttu-id="6de77-164">Aggiunta di foto e video all'elenco dei supporti</span><span class="sxs-lookup"><span data-stu-id="6de77-164">Adding photos and videos to the media list</span></span>

<span data-ttu-id="6de77-165">Il supporto è il fulcro della console multimediale.</span><span class="sxs-lookup"><span data-stu-id="6de77-165">Media is the heart of the Multimedia Console.</span></span>  <span data-ttu-id="6de77-166">Le immagini e i collegamenti video sono supportati come tipi di supporto all'interno della console multimediale.</span><span class="sxs-lookup"><span data-stu-id="6de77-166">Images and video links are supported as media types within the Multimedia Console.</span></span>  <span data-ttu-id="6de77-167">Per aggiungere nuovi supporti, selezionare le icone **Aggiungi immagine** o **Aggiungi video** per visualizzare le informazioni e le impostazioni del supporto.</span><span class="sxs-lookup"><span data-stu-id="6de77-167">To add new media, select either the **Add Image** or **Add Video** icons to have a dialog pop up to enter the media information and settings.</span></span>  <span data-ttu-id="6de77-168">Di seguito è riportata la suddivisione dei tipi di supporto e delle impostazioni associate</span><span class="sxs-lookup"><span data-stu-id="6de77-168">Below is the breakdown of the media types and associated settings</span></span>

<span data-ttu-id="6de77-169">**Immagine**</span><span class="sxs-lookup"><span data-stu-id="6de77-169">**Image**</span></span>

<span data-ttu-id="6de77-170">Le immagini devono essere un tipo di immagine standard, ad esempio JPEG, PNG e figlio.</span><span class="sxs-lookup"><span data-stu-id="6de77-170">Images should be a standard image type such as jpeg, png, and son on.</span></span> <span data-ttu-id="6de77-171">Devono essere ospitati in un punto qualsiasi con un collegamento pubblico.</span><span class="sxs-lookup"><span data-stu-id="6de77-171">They need to be hosted somewhere with a public link.</span></span>

* <span data-ttu-id="6de77-172">**Nome** : (obbligatorio) nome con cui si vuole identificare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="6de77-172">**Name** - (Required) Name that you wish to identify the image with.</span></span>
* <span data-ttu-id="6de77-173">**Image URL** (obbligatorio) URL pubblico dell'immagine</span><span class="sxs-lookup"><span data-stu-id="6de77-173">**Image URL** - (Required) The public url of the image</span></span>
* <span data-ttu-id="6de77-174">**Ignora dopo** : numero di secondi per cui l'immagine deve essere ignorata dopo</span><span class="sxs-lookup"><span data-stu-id="6de77-174">**Skip After** - The number of seconds that the image should be skipped after</span></span>

<span data-ttu-id="6de77-175">**Video**</span><span class="sxs-lookup"><span data-stu-id="6de77-175">**Video**</span></span>

<span data-ttu-id="6de77-176">I video possono essere ospitati video o flussi live tramite contrazione e DLive.</span><span class="sxs-lookup"><span data-stu-id="6de77-176">Videos can be hosted videos or live streams through Twitch and DLive.</span></span>  <span data-ttu-id="6de77-177">(Altri supporto possono funzionare con lavoro aggiuntivo per ottenere l'URL del flusso appropriato, ma non sono completamente supportati nella console multimediale)</span><span class="sxs-lookup"><span data-stu-id="6de77-177">(Other support may function with extra work to get the proper stream url, but aren't fully supported within the Multimedia Console)</span></span>

* <span data-ttu-id="6de77-178">**Nome** : (obbligatorio) nome con cui si vuole identificare il video.</span><span class="sxs-lookup"><span data-stu-id="6de77-178">**Name** - (Required) Name that you wish to identify the video with.</span></span>
* <span data-ttu-id="6de77-179">**URL del video** : (obbligatorio) l'URL pubblico in cui è ospitato il video o da cui viene servito il flusso live.</span><span class="sxs-lookup"><span data-stu-id="6de77-179">**Video URL** - (Required) The public url that the video is hosted at or the live stream is served from.</span></span>
* <span data-ttu-id="6de77-180">**Ignora dopo** : numero di secondi che il video deve ignorare dopo</span><span class="sxs-lookup"><span data-stu-id="6de77-180">**Skip After** - The number of seconds that the video should be skipped after</span></span>
* <span data-ttu-id="6de77-181">**Volume** : volume del video dei valori 0 (min)-1 (max).</span><span class="sxs-lookup"><span data-stu-id="6de77-181">**Volume** - The volume of the video from 0 (min) - 1 (max) values.</span></span>
* <span data-ttu-id="6de77-182">**Ora di inizio** : numero di secondi a partire dall'inizio del video.</span><span class="sxs-lookup"><span data-stu-id="6de77-182">**Start Time** - The number of seconds from the beginning of the video start from.</span></span>
* <span data-ttu-id="6de77-183">**Eseguire il rollback della distanza iniziale** : la distanza in metri nel mondo in cui il volume inizia a uscire dalla console multimediale</span><span class="sxs-lookup"><span data-stu-id="6de77-183">**Roll Off Start Distance** - The distance in meters in world that the volume begins to fall off at as you move away from the Multimedia Console</span></span>
* <span data-ttu-id="6de77-184">**Fine dell'azione video** : azione da eseguire dopo il raggiungimento della fine del video.</span><span class="sxs-lookup"><span data-stu-id="6de77-184">**End of Video Action** - The action to take once the end of the video is reached.</span></span>
    * <span data-ttu-id="6de77-185">Stop-l'elenco dei supporti si interrompe al termine del video</span><span class="sxs-lookup"><span data-stu-id="6de77-185">Stop - The media list stops after the video has ended</span></span>
    * <span data-ttu-id="6de77-186">Loop: il video scorrerà fino a quando non verrà ignorato manualmente</span><span class="sxs-lookup"><span data-stu-id="6de77-186">Loop - The video will loop until manually skipped</span></span>
    * <span data-ttu-id="6de77-187">Riproduci successivo: i supporti successivi nell'elenco di supporti verranno avviati al termine del video corrente.</span><span class="sxs-lookup"><span data-stu-id="6de77-187">Play Next - The next media in the media list will be started after the current video ends.</span></span>

## <a name="working-with-json-directly-advancedoptional"></a><span data-ttu-id="6de77-188">Uso diretto di JSON (Advanced/optional)</span><span class="sxs-lookup"><span data-stu-id="6de77-188">Working with JSON directly (advanced/optional)</span></span>

<span data-ttu-id="6de77-189">La console multimediale supporta l'immissione di codice JSON direttamente nel prompt della console di in AltspaceVR.</span><span class="sxs-lookup"><span data-stu-id="6de77-189">The Multimedia Console supports entering JSON directly in to the prompt of the console in AltspaceVR.</span></span>  <span data-ttu-id="6de77-190">JSON è il meccanismo interno con cui si abilitano le configurazioni di Media Player.</span><span class="sxs-lookup"><span data-stu-id="6de77-190">JSON is the internal mechanism with which we enable media player configurations.</span></span> <span data-ttu-id="6de77-191">Esponendo la possibilità di impostare JSON direttamente è qualcosa che consente agli utenti più avanzati di creare flussi di lavoro personalizzati in grado di soddisfare le proprie esigenze e familiarità con JSON.</span><span class="sxs-lookup"><span data-stu-id="6de77-191">Exposing the ability to set JSON directly is something that allows for more advanced users to build their own workflows that suites their needs and familiarity with JSON.</span></span>  <span data-ttu-id="6de77-192">Di seguito è riportata una breve descrizione della struttura JSON e dello schema in base al quale viene convalidato il JSON.</span><span class="sxs-lookup"><span data-stu-id="6de77-192">The following is a brief description of the JSON structure and the schema by which the JSON is validated.</span></span> <span data-ttu-id="6de77-193">Per descrizioni più dettagliate delle proprietà riportate di seguito, vedere le sezioni precedenti che comunicano sulla configurazione della console multimediale.</span><span class="sxs-lookup"><span data-stu-id="6de77-193">For more detailed descriptions of the properties below, see the above sections that talk about configuring the Multimedia Console.</span></span>  <span data-ttu-id="6de77-194">Questa sezione è incentrata principalmente sugli esempi di schema e sulla strutturazione per i dati JSON.</span><span class="sxs-lookup"><span data-stu-id="6de77-194">This section is focused primarily on the schema examples and structuring for the JSON data.</span></span>

### <a name="global-media-settings"></a><span data-ttu-id="6de77-195">Impostazioni multimediali globali</span><span class="sxs-lookup"><span data-stu-id="6de77-195">Global media settings</span></span>

```json
{
  "loopMediaList": true | false
  "startMethod": "manual" | "autostart-beginning" | "autostart-random"
  "controlMediaPlayer": "everyone" | "elevated" | "owner"
  "configureMediaPlayer": "elevated" | "owner"
  ...
}
```

### <a name="media-list"></a><span data-ttu-id="6de77-196">Elenco supporti</span><span class="sxs-lookup"><span data-stu-id="6de77-196">Media list</span></span>

<span data-ttu-id="6de77-197">L'elenco dei supporti è una proprietà impostata alla radice della struttura JSON, ad esempio i ruoli e le impostazioni di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="6de77-197">The media list is a property set at the root of the JSON structure like the Roles and Playback Settings.</span></span>  <span data-ttu-id="6de77-198">Si tratta di una semplice matrice che può contenere una delle seguenti strutture di configurazione multimediale.</span><span class="sxs-lookup"><span data-stu-id="6de77-198">It's a simple array that can contain one of the following media configuration structures.</span></span> <span data-ttu-id="6de77-199">Per informazioni dettagliate su ciò che accade, vedere le descrizioni delle proprietà precedenti.</span><span class="sxs-lookup"><span data-stu-id="6de77-199">(See property descriptions above for details on what each does.)</span></span>

<span data-ttu-id="6de77-200">**Esempio di immagine**</span><span class="sxs-lookup"><span data-stu-id="6de77-200">**Image example**</span></span>

<span data-ttu-id="6de77-201">*Campi obbligatori: "Name" e "imageUrl"*</span><span class="sxs-lookup"><span data-stu-id="6de77-201">*Required fields: "name" and "imageUrl"*</span></span>

```json
{
    "name": "Altspace Screenshot",
    "imageUrl": "https://pbs.twimg.com/media/CxJ-fJqUsAAFtd9.jpg",
    "skipAfter": 10
}
```

<span data-ttu-id="6de77-202">**Esempio video**</span><span class="sxs-lookup"><span data-stu-id="6de77-202">**Video example**</span></span>

<span data-ttu-id="6de77-203">*Campi obbligatori: "Name" e "videoUrl"*</span><span class="sxs-lookup"><span data-stu-id="6de77-203">*Required fields: "name" and "videoUrl"*</span></span>

```json
{
    "name": "Ninja Twitch Live Stream",
    "videoUrl":"https://www.twitch.tv/ninja",
    "volume":0.2,
    "startTime":0,
    "endOfVideoAction":"play-next"
}
```

### <a name="example-json"></a><span data-ttu-id="6de77-204">JSON di esempio</span><span class="sxs-lookup"><span data-stu-id="6de77-204">Example JSON</span></span>

```json
{
  "loopMediaList": false,
  "startMethod": "autostart-beginning",
  "controlMediaPlayer": "everyone",
  "configureMediaPlayer": "elevated",
  "mediaList": [
    {
      "videoUrl": "https://www.twitch.tv/ninja",
      "volume": 0.2,
      "startTime": 0,
      "endOfVideoAction": "play-next"
    },
    {
      "imageUrl": "http://www.hypergridbusiness.com/wp-content/uploads/2016/09/AltspaceVR-highrise.jpg",
      "skipAfter": 10
    },
    {
      "imageUrl": "https://d1qb2nb5cznatu.cloudfront.net/startups/i/333629-6ffd7199b9bcf34d8957e8e09d974a38-medium_jpg.jpg?buster=1423092095",
      "skipAfter": 5
    },
    {
      "imageUrl": "https://pbs.twimg.com/media/CxJ-fJqUsAAFtd9.jpg",
      "skipAfter": 10
    },
    {
      "imageUrl": "https://altvr-wpengine.netdna-ssl.com/wp-content/uploads/2019/05/Educators-in-VR-Social-VR-AltspaceVR.png",
      "skipAfter": 10
    },
    {
      "videoUrl": "https://www.twitch.tv/shroud",
      "volume": 1,
      "startTime": 0,
      "endOfVideoAction": "stop"
    }
  ]
}
```

### <a name="schema"></a><span data-ttu-id="6de77-205">SCHEMA</span><span class="sxs-lookup"><span data-stu-id="6de77-205">Schema</span></span>

```json
{
  "$schema": "https://json-schema.org/draft-04/schema#",
  "type": "object",
  "required": [
    "mediaList"
  ],
  "properties": {
    "loopMediaList": {
      "type": "boolean",
      "description": "Whether to loop through the media list when reaching the beginning or end of the list."
    },
    "controlMediaPlayer": {
      "type": "string",
      "enum": [
        "everyone",
        "elevated",
        "owner"
      ],
      "default": "owner",
      "description": "What roles are able to control the media player. (Owner can always control player)"
    },
    "configureMediaPlayer": {
      "type": "string",
      "enum": [
        "elevated",
        "owner"
      ],
      "default": "owner",
      "description": "What roles are allowed to configure the media play list.  Note: This role needs to be able to control the media player in order to configure it. (Owner can always configure media)"
    },
    "startMethod": {
      "type": "string",
      "enum": [
        "manual",
        "autostart-beginning",
        "autostart-random"
      ],
      "default": "manual",
      "description": "The method by which the media player should start"
    },
    "mediaList": {
      "description": "A list of images or videos to configure the media player to operate on.",
      "type": "array",
      "items": {
        "oneOf": [
          {
            "title": "Image",
            "type": "object",
            "description": "Configuration for an image media.",
            "properties": {
              "imageUrl": {
                "type": "string",
                "description": "The url for the image to load."
              },
              "skipAfter": {
                "type": "number",
                "minimum": 5,
                "default": null,
                "description": "The number of seconds that should pass before skipping to the next media. (Minimum 5)."
              }
            },
            "required": [
              "imageUrl"
            ]
          },
          {
            "title": "Video",
            "type": "object",
            "description": "Configuration for a video media.",
            "properties": {
              "videoUrl": {
                "type": "string",
                "description": "The url of the video to load."
              },
              "skipAfter": {
                "type": "number",
                "minimum": 5,
                "default": null,
                "description": "The number of seconds that should pass before skipping to the next media. (Minimum 5)."
              },
              "volume": {
                "type": "number",
                "minimum": 0,
                "maximum": 1,
                "default": null,
                "description": "The volume to play the video at. (Minimum 0, maximum 1)"
              },
              "startTime": {
                "type": "number",
                "minimum": 0,
                "default": null,
                "description": "The time in seconds from the start of the video to begin playing the video at. (Minimum of 0)"
              },
              "rolloffStartDistance": {
                "type": "number",
                "minimum": 0,
                "default": null,
                "description": "The distance in meters away from the media player that the volume will begin to fall off. (Minimum 0)"
              },
              "endOfVideoAction": {
                "type": "string",
                "enum": [
                  "stop",
                  "loop",
                  "play-next"
                ],
                "default": null,
                "description": "The type of action to take at the end of the video."
              }
            },
            "required": [
              "videoUrl"
            ]
          }
        ]
      }
    }
  }
}
```

> [!NOTE]
> <span data-ttu-id="6de77-206">Aggiornato con la console multimediale v 0.5.0</span><span class="sxs-lookup"><span data-stu-id="6de77-206">Up to date with Multimedia Console v0.5.0</span></span>