---
title: Uso della console multimediale
description: Informazioni su come iniziare a configurare, pubblicare e controllare la console multimediale nelle esperienze altspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: console, elementi multimediali
ms.openlocfilehash: a24b3700f1687aed6bc00fd218aacd7cc12908e521af6239fac0ae97f48b4b9a
ms.sourcegitcommit: b248ba2a6da7d669b430581fc3a1544413b2e9c1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119127369"
---
# <a name="using-the-multimedia-console"></a>Uso della console multimediale

La console multimediale è uno strumento che consente la condivisione di contenuti multimediali in eventi e mondo. È possibile usarlo per condividere elementi come immagini, diapositive di presentazione, livestream, video, playlist e altro ancora. Di seguito è riportata un'istruzione dettagliata su come usare la console multimediale **v0.5.0+**. 

## <a name="getting-started"></a>Introduzione

L'introduzione alla console multimediale è un processo in due parti.  Prima di tutto è presente il portale Web che verrà utilizzato per generare e pubblicare una configurazione per la sessione della console multimediale che viene posizionata nell'ambiente.  Il secondo è il posizionamento dell'app Console multimediale effettiva nell'ambiente e l'impostazione del codice di configurazione che deve usare.

### <a name="configuring-the-multimedia-console-with-the-web-portal"></a>Configurazione della console multimediale con il portale Web

1. In primo luogo, è necessario assicurarsi che il contenuto sia ospitato online perché è necessario un URL. È possibile caricare foto in un altvr.com, ospitare un file di .mp4 video online o usare un collegamento di streaming live Dlive: https://dlive.tv/yourlivestream) 
2. Passare al portale Web per la Console multimediale all'indirizzo [https://multimedia-console.altvr.com/](https://multimedia-console.altvr.com/)
3. Dal portale Web è possibile generare e pubblicare una configurazione per la console multimediale.  Per informazioni dettagliate sulle varie proprietà, vedere di seguito.
4. Dopo aver immesso i file multimediali nell'elenco dei file multimediali e aver configurato le impostazioni generali, selezionare il pulsante Pubblica nella parte superiore destra dell'app.
5. Al termine della pubblicazione, verrà visualizzata una finestra di dialogo con un codice di due parole da immettere nella console multimediale inserita.
  
### <a name="placing-the-multimedia-console-in-your-environment"></a>Inserimento della console multimediale nell'ambiente

1. Selezionare World **Editor > Editor Panel > SDK Apps > Multimedia Console**. Non passare a World Editor > **Basics > SDK App**(Per le app non registrate).  
2. Posizionare la console multimediale in modo che sia la soluzione migliore per lo spazio e il pubblico.
3. Uscire dalla modalità di modifica facendo clic sul pulsante arancione Modalità di modifica.
4. Verrà chiesto Se si è il **proprietario del lettore multimediale,** Se si è la persona che deve essere il proprietario ufficiale di questa sessione della console multimediale, confermare e continuare. Sono disponibili anche altri ruoli con autorizzazioni. Per un elenco dettagliato, vedere di seguito.
5. Selezionare Sì per confermare di essere l'host primario.  
6. Verrà visualizzata una finestra di dialogo in cui viene chiesto di immettere un codice dal portale Web o json valido.  Immettere il codice delle due parole dal portale Web, incluso il trattino, e fare clic su OK. (JSON è una configurazione avanzata descritta di seguito)
7. La Console multimediale dovrebbe essere caricata dopo alcuni secondi con la configurazione creata nel portale Web.

### <a name="controlling-the-multimedia-console"></a>Controllo della console Multimediale

1. Dopo aver immesso il codice e completato il processo di configurazione, i pulsanti di controllo verranno visualizzati sotto uno schermo multimediale. 
    * **Riproduci** avvia il visualizzatore multimediale (o viene riavviato alla voce corrente, se precedentemente arrestato) 
    * **Arresta** arresta il visualizzatore multimediale e nasconde i file multimediali correnti.  
    * **Next/Prev (Avanti/Prev)** passa al supporto successivo o precedente 
    * **x/x**   mostra l'indice corrente nell'elenco dei supporti e consente di passare a qualsiasi punto dell'elenco
    * **Config** consente di reisferire un nuovo codice dal portale Web per impostare una nuova configurazione nella console. 

A questo punto è possibile iniziare la condivisione tramite la Console multimediale.  
 
## <a name="working-with-the-web-portal"></a>Uso del portale Web

Il portale Web è un'app Web che consente di configurare le varie funzionalità della console multimediale.  Queste funzionalità rientrano in due categorie: impostazioni generali della console multimediale e l'elenco di riproduzione multimediale.

### <a name="multimedia-console-general-settings"></a>Impostazioni generali della console multimediale

**Impostazioni di riproduzione**

Impostazioni generali di riproduzione per l'elenco di file multimediali

* **Loop Media List**(Ciclo elenco supporti) - Determina se l'elenco di supporti deve essere in ciclo quando si raggiunge la fine dell'elenco.
* **Metodo di** avvio: seleziona il metodo con cui deve essere avviata la console multimediale.
    * Manuale: attende che il pulsante di riproduzione venga premuto prima di avviare il supporto
    * Avvio automatico dall'inizio: avvia automaticamente l'elenco di supporti dall'inizio dell'elenco
    * Avvio automatico casuale: avvia automaticamente i supporti da un punto iniziale casuale nell'elenco

**Ruoli**

Assegnazioni di ruolo per il controllo e la configurazione della Console multimediale.    Questi ruoli sono suddivisi nel set seguente:

* **Solo proprietario:** l'utente proprietario della sessione della console multimediale
* **Utenti con privilegi elevati:** utenti che dispongono di ruoli di moderatore o host nello spazio in cui è configurata la console multimediale in origine
* **Tutti gli utenti** - Tutti gli utenti

Questi ruoli si accumulano nel senso che a tutti i ruoli al di sopra di quello scelto in questo elenco verrà concessa anche l'autorizzazione per l'uso di tale funzionalità.  Esempio: **Gli utenti con privilegi elevati** includono il **proprietario** anche se non sono moderatori o host** in AltspaceVR. Le funzionalità controllate dalle assegnazioni di ruolo sono le seguenti:

* **Può controllare il lettore multimediale:** determina quali ruoli possono controllare i pulsanti di riproduzione multimediale per la console multimediale
* **Può configurare il lettore multimediale:** determina quali ruoli possono configurare la console multimediale con l'accesso al **pulsante Config**

### <a name="adding-photos-and-videos-to-the-media-list"></a>Aggiunta di foto e video all'elenco di contenuti multimediali

L'elemento multimediale è il centro della console multimediale.  Le immagini e i collegamenti video sono supportati come tipi di file multimediali all'interno della Console multimediale.  Per aggiungere nuovi file  multimediali, selezionare le icone Aggiungi immagine o Aggiungi **video** per visualizzare una finestra di dialogo in cui immettere le informazioni e le impostazioni relative ai file multimediali.  Di seguito è riportata la suddivisione dei tipi di supporti e delle impostazioni associate

**Immagine**

Le immagini devono essere un tipo di immagine standard, ad esempio jpeg, png e son on. Devono essere ospitati in una posizione con un collegamento pubblico.

* **Nome:** (obbligatorio) Nome con cui si vuole identificare l'immagine.
* **URL immagine:** (obbligatorio) URL pubblico dell'immagine
* **Skip After** (Ignora dopo) - Numero di secondi dopo cui l'immagine deve essere ignorata

**Video**

I video possono essere ospitati in video o flussi live tramite Il tempo e DLive.  Per ottenere l'URL del flusso corretto, è possibile che un altro supporto funzioni con operazioni aggiuntive, ma non sono completamente supportati all'interno della console multimediale.

* **Nome:** (obbligatorio) Nome con cui si vuole identificare il video.
* **URL video:** (obbligatorio) URL pubblico in cui è ospitato il video o da cui viene servito lo streaming live.
* **Skip After** (Ignora dopo) - Numero di secondi dopo cui il video deve essere ignorato

> [!NOTE]
> OBBLIGATORIO: inserire il tempo corrispondente alla lunghezza del video per consentire la corretta inoltro dei video. Ad esempio, se il video è lungo 5 minuti, inserire 300 secondi, in caso contrario il video non verrà ignorato alla parte successiva del contenuto.

* **Volume:** volume del video da 0 (min) - 1 (max) valori.
* **Ora di** inizio: numero di secondi dall'inizio del video.
* **Roll Off Start Distance (Distanza** inizio roll off) - Distanza in metri nel mondo in cui inizia a diminuire il volume quando ci si allontana dalla console multimediale
* **Fine dell'azione** video: azione da eseguire quando viene raggiunta la fine del video.
    * Arresta: l'elenco di contenuti multimediali si arresta al termine del video
    * Ciclo: il video verrà riprodurre in ciclo fino a quando non viene ignorato manualmente
    * Riproduci successivo: gli elementi multimediali successivi nell'elenco dei file multimediali verranno avviati al termine del video corrente.

## <a name="working-with-json-directly-advancedoptional"></a>Uso diretto di JSON (avanzato/facoltativo)

La console multimediale supporta l'immissione di JSON direttamente nel prompt della console in AltspaceVR.  JSON è il meccanismo interno con cui vengono abilitate le configurazioni del lettore multimediale. L'esposizione della possibilità di impostare direttamente JSON è un elemento che consente agli utenti più avanzati di creare flussi di lavoro personalizzati in grado di soddisfare le proprie esigenze e acquisire familiarità con JSON.  Di seguito è riportata una breve descrizione della struttura JSON e dello schema con cui viene convalidato il codice JSON. Per descrizioni più dettagliate delle proprietà riportate di seguito, vedere le sezioni precedenti che descrivono la configurazione della console multimediale.  Questa sezione è incentrata principalmente sugli esempi di schema e sulla strutturazione per i dati JSON.

### <a name="global-media-settings"></a>Impostazioni multimediali globali

```json
{
  "loopMediaList": true | false
  "startMethod": "manual" | "autostart-beginning" | "autostart-random"
  "controlMediaPlayer": "everyone" | "elevated" | "owner"
  "configureMediaPlayer": "elevated" | "owner"
  ...
}
```

### <a name="media-list"></a>Elenco di supporti

L'elenco dei supporti è una proprietà impostata alla radice della struttura JSON, ad esempio roles e playback Impostazioni.  Si tratta di una semplice matrice che può contenere una delle strutture di configurazione dei supporti seguenti. Per informazioni dettagliate sulle relative attività, vedere le descrizioni delle proprietà riportate sopra.

**Esempio di immagine**

*Campi obbligatori: "name" e "imageUrl"*

```json
{
    "name": "Altspace Screenshot",
    "imageUrl": "https://pbs.twimg.com/media/CxJ-fJqUsAAFtd9.jpg",
    "skipAfter": 10
}
```

**Esempio di video**

*Campi obbligatori: "name" e "videoUrl"*

```json
{
    "name": "Ninja Twitch Live Stream",
    "videoUrl":"https://www.twitch.tv/ninja",
    "volume":0.2,
    "startTime":0,
    "endOfVideoAction":"play-next"
}
```

### <a name="example-json"></a>JSON di esempio

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

### <a name="schema"></a>Schema

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
> Aggiornato con La console multimediale v0.5.0