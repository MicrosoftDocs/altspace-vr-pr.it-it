---
title: Uso della console multimediale
description: Informazioni su come iniziare a configurare, pubblicare e controllare la console multimediale nelle esperienze altspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: console, elementi multimediali
ms.openlocfilehash: 4a51ff76e44d3870972bc17288ae77c1fa888922
ms.sourcegitcommit: 2db596ab5a1ecd4901a8c893741cc4d06f6aecea
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/25/2021
ms.locfileid: "112923008"
---
# <a name="using-the-multimedia-console"></a><span data-ttu-id="a7ba6-104">Uso della console multimediale</span><span class="sxs-lookup"><span data-stu-id="a7ba6-104">Using the multimedia console</span></span>

<span data-ttu-id="a7ba6-105">La console multimediale è uno strumento che consente la condivisione di contenuti multimediali in eventi e mondo.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-105">The Multimedia Console is a tool that enables media sharing in events and worlds.</span></span> <span data-ttu-id="a7ba6-106">È possibile usarlo per condividere elementi come immagini, diapositive di presentazione, livestream, video, playlist e altro ancora.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-106">You can use it to share things like images, presentation slides, livestreams, videos, playlists, and more.</span></span> <span data-ttu-id="a7ba6-107">Di seguito è riportata un'istruzione dettagliata su come usare la console multimediale **v0.5.0+**.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-107">Below is a step-by-step instruction on how to use the Multimedia Console **v0.5.0+**.</span></span> 

## <a name="getting-started"></a><span data-ttu-id="a7ba6-108">Guida introduttiva</span><span class="sxs-lookup"><span data-stu-id="a7ba6-108">Getting started</span></span>

<span data-ttu-id="a7ba6-109">L'introduzione alla console multimediale è un processo in due parti.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-109">Getting started with the Multimedia Console is a two part process.</span></span>  <span data-ttu-id="a7ba6-110">Prima di tutto è presente il portale Web che verrà utilizzato per generare e pubblicare una configurazione per la sessione della console multimediale che viene posizionata nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-110">First there's the web portal that you'll use to generate and publish a configuration for the Multimedia Console session you place in your environment.</span></span>  <span data-ttu-id="a7ba6-111">Il secondo è il posizionamento dell'app Console multimediale effettiva nell'ambiente e l'impostazione del codice di configurazione che deve usare.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-111">Second is the placement of the actual Multimedia Console app in your environment and setting the configuration code it should use.</span></span>

### <a name="configuring-the-multimedia-console-with-the-web-portal"></a><span data-ttu-id="a7ba6-112">Configurazione della console Multimediale con il portale Web</span><span class="sxs-lookup"><span data-stu-id="a7ba6-112">Configuring the Multimedia console with the web portal</span></span>

1. <span data-ttu-id="a7ba6-113">Prima di tutto, è necessario assicurarsi che il contenuto sia ospitato online perché è necessario un URL.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-113">First, you'll need to make sure your content is hosted online because you'll need a URL.</span></span> <span data-ttu-id="a7ba6-114">È possibile caricare foto in un altvr.com, ospitare un file di .mp4 video online o usare un collegamento di streaming live Dlive: https://dlive.tv/yourlivestream)</span><span class="sxs-lookup"><span data-stu-id="a7ba6-114">(You can upload photos to altvr.com, host a video .mp4 file online or use a Dlive live stream link: https://dlive.tv/yourlivestream)</span></span> 
2. <span data-ttu-id="a7ba6-115">Passare al portale Web per la Console multimediale all'indirizzo [https://multimedia-console.altvr.com/](https://multimedia-console.altvr.com/)</span><span class="sxs-lookup"><span data-stu-id="a7ba6-115">Navigate to the web portal for the Multimedia Console at [https://multimedia-console.altvr.com/](https://multimedia-console.altvr.com/)</span></span>
3. <span data-ttu-id="a7ba6-116">Dal portale Web è possibile generare e pubblicare una configurazione per la console multimediale.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-116">From the web portal, you can generate and publish a configuration for the Multimedia Console.</span></span>  <span data-ttu-id="a7ba6-117">Per informazioni dettagliate sulle varie proprietà, vedere di seguito.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-117">(See below for details about the various properties).</span></span>
4. <span data-ttu-id="a7ba6-118">Dopo aver immesso i file multimediali nell'elenco dei file multimediali e aver configurato le impostazioni generali, selezionare il pulsante Pubblica nella parte superiore destra dell'app.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-118">Once you've entered the media into the media list and have configured the general settings, select the publish button in the top-right part of the app.</span></span>
5. <span data-ttu-id="a7ba6-119">Al termine della pubblicazione, verrà visualizzata una finestra di dialogo con un codice di due parole da immettere nella console multimediale inserita.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-119">Once the publish has completed, a dialog will pop up with a two word code for you to enter in to the Multimedia Console you placed.</span></span>
  
### <a name="placing-the-multimedia-console-in-your-environment"></a><span data-ttu-id="a7ba6-120">Inserimento della console Multimediale nell'ambiente</span><span class="sxs-lookup"><span data-stu-id="a7ba6-120">Placing the Multimedia console in your environment</span></span>

1. <span data-ttu-id="a7ba6-121">Selezionare World **Editor > Editor Panel > SDK Apps > Multimedia Console**.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-121">Select on **World Editor > Editor Panel > SDK Apps > Multimedia Console**.</span></span> <span data-ttu-id="a7ba6-122">Non passare a World Editor > **Basics > SDK App**(Per le app non registrate).</span><span class="sxs-lookup"><span data-stu-id="a7ba6-122">(Don't go to **World Editor > Basics > SDK App**--that's for unregistered apps.)</span></span>  
2. <span data-ttu-id="a7ba6-123">Posizionare la console multimediale in modo che sia la soluzione migliore per lo spazio e il pubblico.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-123">Position the Multimedia Console to best suite your space and audience.</span></span>
3. <span data-ttu-id="a7ba6-124">Uscire dalla modalità di modifica facendo clic sul pulsante arancione Modalità di modifica.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-124">Get out of Edit Mode by clicking the orange Edit Mode button.</span></span>
4. <span data-ttu-id="a7ba6-125">Verrà chiesto Se si è il **proprietario del lettore multimediale,**</span><span class="sxs-lookup"><span data-stu-id="a7ba6-125">You'll be prompted **Are you the media player owner?**</span></span> <span data-ttu-id="a7ba6-126">Se si è la persona che deve essere il proprietario ufficiale di questa sessione della console multimediale, confermare e continuare.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-126">If you're the person who should be the official owner of this Multimedia Console session, confirm and continue.</span></span> <span data-ttu-id="a7ba6-127">Sono disponibili anche altri ruoli con autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-127">(Other permissioned roles are available as well.</span></span> <span data-ttu-id="a7ba6-128">Per un elenco dettagliato, vedere di seguito.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-128">See below for a detailed list.)</span></span>
5. <span data-ttu-id="a7ba6-129">Selezionare Sì per confermare di essere l'host primario.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-129">Select Yes to confirm that you are the primary host.</span></span>  
6. <span data-ttu-id="a7ba6-130">Verrà visualizzata una finestra di dialogo in cui viene chiesto di immettere un codice dal portale Web o un codice JSON valido.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-130">A dialog should pop up that asks you to enter a code from the web portal or valid JSON.</span></span>  <span data-ttu-id="a7ba6-131">Immettere il codice delle due parole dal portale Web, incluso il trattino, e fare clic su OK.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-131">Enter the two word code from the web portal including the dash and hit OK.</span></span> <span data-ttu-id="a7ba6-132">(JSON è una configurazione avanzata descritta di seguito)</span><span class="sxs-lookup"><span data-stu-id="a7ba6-132">(JSON is an advanced configuration described below)</span></span>
7. <span data-ttu-id="a7ba6-133">La Console multimediale dovrebbe essere caricata dopo alcuni secondi con la configurazione creata nel portale Web.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-133">The Multimedia Console should load after a few seconds with the configuration you built in the web portal.</span></span>

### <a name="controlling-the-multimedia-console"></a><span data-ttu-id="a7ba6-134">Controllo della console Multimediale</span><span class="sxs-lookup"><span data-stu-id="a7ba6-134">Controlling the Multimedia console</span></span>

1. <span data-ttu-id="a7ba6-135">Dopo aver immesso il codice e completato il processo di configurazione, i pulsanti di controllo verranno visualizzati sotto uno schermo multimediale.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-135">After you input your code and complete the configuration process, you'll see control buttons appear below a media display.</span></span> 
    * <span data-ttu-id="a7ba6-136">**Riproduci** avvia il visualizzatore multimediale (o viene riavviato alla voce corrente, se precedentemente arrestato)</span><span class="sxs-lookup"><span data-stu-id="a7ba6-136">**Play** starts the media viewer (or restarts at current entry, if previously stopped)</span></span> 
    * <span data-ttu-id="a7ba6-137">**Arresta** arresta il visualizzatore multimediale e nasconde i file multimediali correnti.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-137">**Stop** stops the media viewer, and hides current media.</span></span>  
    * <span data-ttu-id="a7ba6-138">**Next/Prev (Avanti/Prev)** passa al supporto successivo o precedente</span><span class="sxs-lookup"><span data-stu-id="a7ba6-138">**Next/Prev** skips to next or previous media</span></span> 
    * <span data-ttu-id="a7ba6-139">**x/x**   mostra l'indice corrente nell'elenco dei supporti e consente di passare a qualsiasi punto dell'elenco</span><span class="sxs-lookup"><span data-stu-id="a7ba6-139">**x/x** shows the current index into the media list, and allows you to jump to any point in the list</span></span>
    * <span data-ttu-id="a7ba6-140">**Config** consente di rientrare in un nuovo codice dal portale Web per impostare una nuova configurazione nella console.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-140">**Config** allows reentering a new code from the web portal to set a new configuration in the console.</span></span> 

<span data-ttu-id="a7ba6-141">A questo punto è possibile iniziare la condivisione tramite la console multimediale.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-141">Now you're set to begin sharing via the Multimedia Console!</span></span>  
 
## <a name="working-with-the-web-portal"></a><span data-ttu-id="a7ba6-142">Uso del portale Web</span><span class="sxs-lookup"><span data-stu-id="a7ba6-142">Working with the web portal</span></span>

<span data-ttu-id="a7ba6-143">Il portale Web è un'app Web che consente di configurare le varie funzionalità della console multimediale.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-143">The web portal is a web app that enables configuring the various features of the Multimedia Console.</span></span>  <span data-ttu-id="a7ba6-144">Queste funzionalità rientrano in due categorie: impostazioni generali della console multimediale e l'elenco di riproduzione multimediale.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-144">These features fall in to two categories; general media console settings, and the media play list.</span></span>

### <a name="multimedia-console-general-settings"></a><span data-ttu-id="a7ba6-145">Impostazioni generali della console multimediale</span><span class="sxs-lookup"><span data-stu-id="a7ba6-145">Multimedia console general settings</span></span>

<span data-ttu-id="a7ba6-146">**Impostazioni di riproduzione**</span><span class="sxs-lookup"><span data-stu-id="a7ba6-146">**Playback Settings**</span></span>

<span data-ttu-id="a7ba6-147">Impostazioni generali di riproduzione per l'elenco di file multimediali</span><span class="sxs-lookup"><span data-stu-id="a7ba6-147">General playback settings for the media list</span></span>

* <span data-ttu-id="a7ba6-148">**Loop Media List**(Ciclo elenco supporti) - Determina se l'elenco di supporti deve essere in ciclo quando si raggiunge la fine dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-148">**Loop Media List**- Determines whether the media list should loop around once you reach the end of the list.</span></span>
* <span data-ttu-id="a7ba6-149">**Metodo start:** seleziona il metodo con cui deve essere avviata la console multimediale.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-149">**Start Method** - Selects the method by which the multimedia console should start.</span></span>
    * <span data-ttu-id="a7ba6-150">Manuale: attende che il pulsante di riproduzione venga premuto prima di avviare il supporto</span><span class="sxs-lookup"><span data-stu-id="a7ba6-150">Manual - Waits for the play button to be pressed before starting the media</span></span>
    * <span data-ttu-id="a7ba6-151">Avvio automatico dall'inizio: avvia automaticamente l'elenco di supporti dall'inizio dell'elenco</span><span class="sxs-lookup"><span data-stu-id="a7ba6-151">Auto Start from Beginning - Auto start the media list from the beginning of the list</span></span>
    * <span data-ttu-id="a7ba6-152">Avvio automatico casuale: avvia automaticamente i supporti da un punto iniziale casuale nell'elenco</span><span class="sxs-lookup"><span data-stu-id="a7ba6-152">Auto Start Random - Auto starts the media from a random starting point in the list</span></span>

<span data-ttu-id="a7ba6-153">**Ruoli**</span><span class="sxs-lookup"><span data-stu-id="a7ba6-153">**Roles**</span></span>

<span data-ttu-id="a7ba6-154">Assegnazioni di ruolo per il controllo e la configurazione della Console multimediale.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-154">Role assignments for controlling and configuring the Multimedia Console.</span></span>    <span data-ttu-id="a7ba6-155">Questi ruoli sono suddivisi nel set seguente:</span><span class="sxs-lookup"><span data-stu-id="a7ba6-155">These roles are broken down in to the following set:</span></span>

* <span data-ttu-id="a7ba6-156">**Solo proprietario:** l'utente proprietario della sessione della console multimediale</span><span class="sxs-lookup"><span data-stu-id="a7ba6-156">**Owner Only** - The user that is the owner of the Multimedia Console Session</span></span>
* <span data-ttu-id="a7ba6-157">**Utenti con privilegi elevati:** utenti che dispongono di ruoli di moderatore o host nello spazio in cui è configurata la console multimediale in origine</span><span class="sxs-lookup"><span data-stu-id="a7ba6-157">**Elevated Users** - Users that have moderator or host roles in the space that the Multimedia Console is configured in originally</span></span>
* <span data-ttu-id="a7ba6-158">**Tutti gli utenti** - Tutti gli utenti</span><span class="sxs-lookup"><span data-stu-id="a7ba6-158">**All Users** - All users</span></span>

<span data-ttu-id="a7ba6-159">Questi ruoli si accumulano nel senso che a tutti i ruoli al di sopra di quello scelto in questo elenco verrà concessa anche l'autorizzazione per l'uso di tale funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-159">These roles stack in the sense that all roles above the one chosen in this list will also be granted permission to use that feature.</span></span>  <span data-ttu-id="a7ba6-160">Esempio: **Gli utenti con privilegi elevati** includono il **proprietario** anche se non sono moderatori o host\*\* in AltspaceVR.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-160">Example: **Elevated Users** includes the **Owner** even if they aren't a moderator or host\*\* in AltspaceVR.</span></span> <span data-ttu-id="a7ba6-161">Le funzionalità controllate dalle assegnazioni di ruolo sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="a7ba6-161">Features that are controlled by role assignments are as follows</span></span>

* <span data-ttu-id="a7ba6-162">**Può controllare il lettore multimediale:** determina quali ruoli possono controllare i pulsanti di riproduzione multimediale per la console multimediale</span><span class="sxs-lookup"><span data-stu-id="a7ba6-162">**Can control media player** - Determines what roles can control the media playback buttons for the Multimedia Console</span></span>
* <span data-ttu-id="a7ba6-163">**Può configurare il lettore multimediale:** determina i ruoli che possono configurare la console multimediale tramite la concessione dell'accesso al **pulsante Config**</span><span class="sxs-lookup"><span data-stu-id="a7ba6-163">**Can configure the media player** - Determines what roles can configure the Multimedia Console by being granted access to the **Config** button</span></span>

### <a name="adding-photos-and-videos-to-the-media-list"></a><span data-ttu-id="a7ba6-164">Aggiunta di foto e video all'elenco di contenuti multimediali</span><span class="sxs-lookup"><span data-stu-id="a7ba6-164">Adding photos and videos to the media list</span></span>

<span data-ttu-id="a7ba6-165">L'elemento multimediale è il centro della console multimediale.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-165">Media is the heart of the Multimedia Console.</span></span>  <span data-ttu-id="a7ba6-166">Le immagini e i collegamenti video sono supportati come tipi di file multimediali all'interno della Console multimediale.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-166">Images and video links are supported as media types within the Multimedia Console.</span></span>  <span data-ttu-id="a7ba6-167">Per aggiungere nuovi file  multimediali, selezionare le icone Aggiungi immagine o Aggiungi **video** per visualizzare una finestra di dialogo in cui immettere le informazioni e le impostazioni relative ai file multimediali.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-167">To add new media, select either the **Add Image** or **Add Video** icons to have a dialog pop up to enter the media information and settings.</span></span>  <span data-ttu-id="a7ba6-168">Di seguito è riportata la suddivisione dei tipi di supporti e delle impostazioni associate</span><span class="sxs-lookup"><span data-stu-id="a7ba6-168">Below is the breakdown of the media types and associated settings</span></span>

<span data-ttu-id="a7ba6-169">**Immagine**</span><span class="sxs-lookup"><span data-stu-id="a7ba6-169">**Image**</span></span>

<span data-ttu-id="a7ba6-170">Le immagini devono essere un tipo di immagine standard, ad esempio jpeg, png e son on.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-170">Images should be a standard image type such as jpeg, png, and son on.</span></span> <span data-ttu-id="a7ba6-171">Devono essere ospitati in una posizione con un collegamento pubblico.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-171">They need to be hosted somewhere with a public link.</span></span>

* <span data-ttu-id="a7ba6-172">**Nome:** (obbligatorio) Nome con cui si vuole identificare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-172">**Name** - (Required) Name that you wish to identify the image with.</span></span>
* <span data-ttu-id="a7ba6-173">**URL immagine:** (obbligatorio) URL pubblico dell'immagine</span><span class="sxs-lookup"><span data-stu-id="a7ba6-173">**Image URL** - (Required) The public url of the image</span></span>
* <span data-ttu-id="a7ba6-174">**Skip After** (Ignora dopo) - Numero di secondi dopo cui l'immagine deve essere ignorata</span><span class="sxs-lookup"><span data-stu-id="a7ba6-174">**Skip After** - The number of seconds that the image should be skipped after</span></span>

<span data-ttu-id="a7ba6-175">**Video**</span><span class="sxs-lookup"><span data-stu-id="a7ba6-175">**Video**</span></span>

<span data-ttu-id="a7ba6-176">I video possono essere ospitati in video o in streaming live tramite Iaa e DLive.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-176">Videos can be hosted videos or live streams through Twitch and DLive.</span></span>  <span data-ttu-id="a7ba6-177">Per ottenere l'URL del flusso corretto, è possibile che altri supportino operazioni aggiuntive, ma non siano completamente supportati all'interno della console multimediale.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-177">(Other support may function with extra work to get the proper stream url, but aren't fully supported within the Multimedia Console)</span></span>

* <span data-ttu-id="a7ba6-178">**Nome:** (obbligatorio) Nome con cui si vuole identificare il video.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-178">**Name** - (Required) Name that you wish to identify the video with.</span></span>
* <span data-ttu-id="a7ba6-179">**URL video:** (obbligatorio) URL pubblico in cui è ospitato il video o da cui viene servito lo streaming live.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-179">**Video URL** - (Required) The public url that the video is hosted at or the live stream is served from.</span></span>
* <span data-ttu-id="a7ba6-180">**Skip After** (Ignora dopo) - Numero di secondi dopo cui il video deve essere ignorato</span><span class="sxs-lookup"><span data-stu-id="a7ba6-180">**Skip After** - The number of seconds that the video should be skipped after</span></span>

> [!NOTE]
> <span data-ttu-id="a7ba6-181">OBBLIGATORIO: inserire il tempo corrispondente alla lunghezza del video per consentire l'inoltro corretto dei video.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-181">REQUIRED: Put in the time that matches the length of the video to enable videos to properly forward.</span></span> <span data-ttu-id="a7ba6-182">Ad esempio, se il video ha una durata di 5 minuti, inserire 300 secondi, altrimenti il video non verrà ignorato al contenuto successivo.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-182">For example, if your video is 5 minutes long put 300 seconds, otherwise your video won't skip to the next piece of content.</span></span>

* <span data-ttu-id="a7ba6-183">**Volume:** volume del video da 0 (min) - 1 (max) valori.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-183">**Volume** - The volume of the video from 0 (min) - 1 (max) values.</span></span>
* <span data-ttu-id="a7ba6-184">**Ora di** inizio: numero di secondi dall'inizio del video.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-184">**Start Time** - The number of seconds from the beginning of the video start from.</span></span>
* <span data-ttu-id="a7ba6-185">**Roll Off Start Distance (Distanza** inizio roll off) - Distanza in metri nel mondo in cui inizia a diminuire il volume quando ci si allontana dalla console multimediale</span><span class="sxs-lookup"><span data-stu-id="a7ba6-185">**Roll Off Start Distance** - The distance in meters in world that the volume begins to fall off at as you move away from the Multimedia Console</span></span>
* <span data-ttu-id="a7ba6-186">**Fine dell'azione** video: azione da eseguire quando viene raggiunta la fine del video.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-186">**End of Video Action** - The action to take once the end of the video is reached.</span></span>
    * <span data-ttu-id="a7ba6-187">Arresta: l'elenco di contenuti multimediali si arresta al termine del video</span><span class="sxs-lookup"><span data-stu-id="a7ba6-187">Stop - The media list stops after the video has ended</span></span>
    * <span data-ttu-id="a7ba6-188">Ciclo: il video verrà riprodurre in ciclo fino a quando non viene ignorato manualmente</span><span class="sxs-lookup"><span data-stu-id="a7ba6-188">Loop - The video will loop until manually skipped</span></span>
    * <span data-ttu-id="a7ba6-189">Riproduci successivo: gli elementi multimediali successivi nell'elenco dei file multimediali verranno avviati al termine del video corrente.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-189">Play Next - The next media in the media list will be started after the current video ends.</span></span>

## <a name="working-with-json-directly-advancedoptional"></a><span data-ttu-id="a7ba6-190">Uso diretto di JSON (avanzato/facoltativo)</span><span class="sxs-lookup"><span data-stu-id="a7ba6-190">Working with JSON directly (advanced/optional)</span></span>

<span data-ttu-id="a7ba6-191">La console multimediale supporta l'immissione di JSON direttamente nel prompt della console in AltspaceVR.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-191">The Multimedia Console supports entering JSON directly in to the prompt of the console in AltspaceVR.</span></span>  <span data-ttu-id="a7ba6-192">JSON è il meccanismo interno con cui vengono abilitate le configurazioni del lettore multimediale.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-192">JSON is the internal mechanism with which we enable media player configurations.</span></span> <span data-ttu-id="a7ba6-193">L'esposizione della possibilità di impostare direttamente JSON è un elemento che consente agli utenti più avanzati di creare flussi di lavoro personalizzati in grado di soddisfare le proprie esigenze e acquisire familiarità con JSON.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-193">Exposing the ability to set JSON directly is something that allows for more advanced users to build their own workflows that suites their needs and familiarity with JSON.</span></span>  <span data-ttu-id="a7ba6-194">Di seguito è riportata una breve descrizione della struttura JSON e dello schema con cui viene convalidato il codice JSON.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-194">The following is a brief description of the JSON structure and the schema by which the JSON is validated.</span></span> <span data-ttu-id="a7ba6-195">Per descrizioni più dettagliate delle proprietà riportate di seguito, vedere le sezioni precedenti che descrivono la configurazione della console multimediale.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-195">For more detailed descriptions of the properties below, see the above sections that talk about configuring the Multimedia Console.</span></span>  <span data-ttu-id="a7ba6-196">Questa sezione è incentrata principalmente sugli esempi di schema e sulla strutturazione per i dati JSON.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-196">This section is focused primarily on the schema examples and structuring for the JSON data.</span></span>

### <a name="global-media-settings"></a><span data-ttu-id="a7ba6-197">Impostazioni multimediali globali</span><span class="sxs-lookup"><span data-stu-id="a7ba6-197">Global media settings</span></span>

```json
{
  "loopMediaList": true | false
  "startMethod": "manual" | "autostart-beginning" | "autostart-random"
  "controlMediaPlayer": "everyone" | "elevated" | "owner"
  "configureMediaPlayer": "elevated" | "owner"
  ...
}
```

### <a name="media-list"></a><span data-ttu-id="a7ba6-198">Elenco di supporti</span><span class="sxs-lookup"><span data-stu-id="a7ba6-198">Media list</span></span>

<span data-ttu-id="a7ba6-199">L'elenco dei supporti è una proprietà impostata alla radice della struttura JSON, ad esempio Ruoli e Impostazioni di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-199">The media list is a property set at the root of the JSON structure like the Roles and Playback Settings.</span></span>  <span data-ttu-id="a7ba6-200">Si tratta di una semplice matrice che può contenere una delle strutture di configurazione dei supporti seguenti.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-200">It's a simple array that can contain one of the following media configuration structures.</span></span> <span data-ttu-id="a7ba6-201">Per informazioni dettagliate sulle relative attività, vedere le descrizioni delle proprietà riportate sopra.</span><span class="sxs-lookup"><span data-stu-id="a7ba6-201">(See property descriptions above for details on what each does.)</span></span>

<span data-ttu-id="a7ba6-202">**Esempio di immagine**</span><span class="sxs-lookup"><span data-stu-id="a7ba6-202">**Image example**</span></span>

<span data-ttu-id="a7ba6-203">*Campi obbligatori: "name" e "imageUrl"*</span><span class="sxs-lookup"><span data-stu-id="a7ba6-203">*Required fields: "name" and "imageUrl"*</span></span>

```json
{
    "name": "Altspace Screenshot",
    "imageUrl": "https://pbs.twimg.com/media/CxJ-fJqUsAAFtd9.jpg",
    "skipAfter": 10
}
```

<span data-ttu-id="a7ba6-204">**Esempio di video**</span><span class="sxs-lookup"><span data-stu-id="a7ba6-204">**Video example**</span></span>

<span data-ttu-id="a7ba6-205">*Campi obbligatori: "name" e "videoUrl"*</span><span class="sxs-lookup"><span data-stu-id="a7ba6-205">*Required fields: "name" and "videoUrl"*</span></span>

```json
{
    "name": "Ninja Twitch Live Stream",
    "videoUrl":"https://www.twitch.tv/ninja",
    "volume":0.2,
    "startTime":0,
    "endOfVideoAction":"play-next"
}
```

### <a name="example-json"></a><span data-ttu-id="a7ba6-206">JSON di esempio</span><span class="sxs-lookup"><span data-stu-id="a7ba6-206">Example JSON</span></span>

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

### <a name="schema"></a><span data-ttu-id="a7ba6-207">SCHEMA</span><span class="sxs-lookup"><span data-stu-id="a7ba6-207">Schema</span></span>

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
> <span data-ttu-id="a7ba6-208">Aggiornato con La console multimediale v0.5.0</span><span class="sxs-lookup"><span data-stu-id="a7ba6-208">Up to date with Multimedia Console v0.5.0</span></span>