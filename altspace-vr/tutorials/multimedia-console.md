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
# <a name="using-the-multimedia-console"></a>Uso della console multimediale

La console multimediale è uno strumento che consente la condivisione di contenuti multimediali in eventi e mondi. È possibile usarlo per condividere elementi quali immagini, diapositive di presentazione, Livestream, video, playlist e altro ancora. Di seguito sono riportate istruzioni dettagliate su come usare la console multimediale **v 0.5.0 +**. 

## <a name="getting-started"></a>Introduzione

La Guida introduttiva alla console multimediale è un processo in due parti.  Per prima cosa, è disponibile il portale Web che verrà usato per generare e pubblicare una configurazione per la sessione della console multimediale che viene posizionata nell'ambiente.  Il secondo è la posizione dell'app console multimediale effettiva nell'ambiente e l'impostazione del codice di configurazione da usare.

### <a name="configuring-the-multimedia-console-with-the-web-portal"></a>Configurazione della console multimediale con il portale Web

1. Prima di tutto, è necessario assicurarsi che il contenuto sia ospitato online perché è necessario un URL. (È possibile caricare le foto in altvr.com, ospitare un file video. MP4 in linea o usare il collegamento di streaming live: https://www.twitch.tv/ninja) 
2. Passare al portale Web per la console multimediale all'indirizzo [https://multimedia-console.altvr.com/](https://multimedia-console.altvr.com/)
3. Dal portale Web è possibile generare e pubblicare una configurazione per la console multimediale.  (Vedere di seguito per informazioni dettagliate sulle varie proprietà).
4. Dopo aver immesso il supporto nell'elenco dei supporti e aver configurato le impostazioni generali, selezionare il pulsante pubblica nella parte superiore destra dell'app.
5. Una volta completata la pubblicazione, viene visualizzata una finestra di dialogo con un codice di due parole per poter accedere alla console multimediale inserita.
  
### <a name="placing-the-multimedia-console-in-your-environment"></a>Inserimento della console multimediale nell'ambiente

1. Selezionare nel **Pannello editor > editor del mondo > App SDK > console multimediale**. Non passare all' **editor globale > nozioni di base > App SDK**, ovvero per le app non registrate.  
2. Posizionare la console multimediale per la migliore suite di spazio e destinatari.
3. Per uscire dalla modalità di modifica, fare clic sul pulsante arancione della modalità di modifica.
4. Verrà richiesto di immettere **il proprietario del Media Player?** Se si è l'utente che deve essere il proprietario ufficiale della sessione della console multimediale, confermare e continuare. Sono disponibili anche altri ruoli con autorizzazioni. Per un elenco dettagliato, vedere di seguito.
5. Selezionare Sì per confermare che si è l'host primario.  
6. Verrà visualizzata una finestra di dialogo che richiede di immettere un codice dal portale Web o da JSON valido.  Immettere il codice di due parole dal portale Web, incluso il trattino, e fare clic su OK. (JSON è una configurazione avanzata descritta di seguito)
7. La console multimediale dovrebbe essere caricata dopo alcuni secondi con la configurazione creata nel portale Web.

### <a name="controlling-the-multimedia-console"></a>Controllo della console multimediale

1. Dopo aver inserito il codice e completato il processo di configurazione, verranno visualizzati i pulsanti di controllo sotto uno schermo multimediale. 
    * **Play** avvia il Visualizzatore multimediale (o riavvia in corrispondenza della voce corrente, se in precedenza è stato arrestato) 
    * **Stop** arresta il Visualizzatore multimediale e nasconde i supporti correnti.  
    * **Avanti/indietro** ignora i supporti successivi o precedenti 
    * **x/x**   Mostra l'indice corrente nell'elenco dei supporti e consente di passare a un punto qualsiasi dell'elenco
    * **Config** consente di reimmettere un nuovo codice dal portale Web per impostare una nuova configurazione nella console di. 

A questo punto è possibile iniziare la condivisione tramite la console multimediale.  
 
## <a name="working-with-the-web-portal"></a>Uso del portale Web

Il portale Web è un'app Web che consente di configurare le varie funzionalità della console multimediale.  Queste funzionalità rientrino in due categorie: impostazioni generali della console multimediale e Media Play List.

### <a name="multimedia-console-general-settings"></a>Impostazioni generali della console multimediale

**Impostazioni di riproduzione**

Impostazioni di riproduzione generale per l'elenco dei supporti

* **Elenco supporti ciclo**: determina se l'elenco dei supporti deve essere in loop una volta raggiunta la fine dell'elenco.
* **Metodo Start** : seleziona il metodo in base al quale deve essere avviata la console multimediale.
    * Manual: attende che venga premuto il pulsante Play prima di avviare il supporto
    * Avvio automatico dall'inizio-avvio automatico dell'elenco dei supporti dall'inizio dell'elenco
    * Avvio automatico casuale: avvia automaticamente il supporto da un punto di partenza casuale nell'elenco

**Ruoli**

Assegnazioni di ruolo per il controllo e la configurazione della console multimediale.    Questi ruoli sono suddivisi nel seguente set:

* **Solo proprietario** : l'utente proprietario della sessione della console multimediale
* **Utenti con privilegi elevati** : utenti con ruoli di moderatore, host o Presenter nello spazio in cui la console multimediale è configurata originariamente
* **Tutti gli utenti** -tutti gli utenti

Questo stack di ruoli nel senso che a tutti i ruoli sopra a quello scelto in questo elenco verrà inoltre concessa l'autorizzazione per l'utilizzo di tale funzionalità.  Esempio: **gli utenti con privilegi elevati** includono il **proprietario** anche se non sono un moderatore, un host o un presentatore * * in AltspaceVR. Di seguito sono riportate le funzionalità controllate dalle assegnazioni di ruolo

* **Consente di controllare il lettore multimediale** : determina quali ruoli possono controllare i pulsanti di riproduzione dei supporti per la console multimediale
* **Può configurare Media Player** : determina i ruoli che possono configurare la console multimediale, a cui viene concesso l'accesso al pulsante **config**

### <a name="adding-photos-and-videos-to-the-media-list"></a>Aggiunta di foto e video all'elenco dei supporti

Il supporto è il fulcro della console multimediale.  Le immagini e i collegamenti video sono supportati come tipi di supporto all'interno della console multimediale.  Per aggiungere nuovi supporti, selezionare le icone **Aggiungi immagine** o **Aggiungi video** per visualizzare le informazioni e le impostazioni del supporto.  Di seguito è riportata la suddivisione dei tipi di supporto e delle impostazioni associate

**Immagine**

Le immagini devono essere un tipo di immagine standard, ad esempio JPEG, PNG e figlio. Devono essere ospitati in un punto qualsiasi con un collegamento pubblico.

* **Nome** : (obbligatorio) nome con cui si vuole identificare l'immagine.
* **Image URL** (obbligatorio) URL pubblico dell'immagine
* **Ignora dopo** : numero di secondi per cui l'immagine deve essere ignorata dopo

**Video**

I video possono essere ospitati video o flussi live tramite contrazione e DLive.  (Altri supporto possono funzionare con lavoro aggiuntivo per ottenere l'URL del flusso appropriato, ma non sono completamente supportati nella console multimediale)

* **Nome** : (obbligatorio) nome con cui si vuole identificare il video.
* **URL del video** : (obbligatorio) l'URL pubblico in cui è ospitato il video o da cui viene servito il flusso live.
* **Ignora dopo** : numero di secondi che il video deve ignorare dopo
* **Volume** : volume del video dei valori 0 (min)-1 (max).
* **Ora di inizio** : numero di secondi a partire dall'inizio del video.
* **Eseguire il rollback della distanza iniziale** : la distanza in metri nel mondo in cui il volume inizia a uscire dalla console multimediale
* **Fine dell'azione video** : azione da eseguire dopo il raggiungimento della fine del video.
    * Stop-l'elenco dei supporti si interrompe al termine del video
    * Loop: il video scorrerà fino a quando non verrà ignorato manualmente
    * Riproduci successivo: i supporti successivi nell'elenco di supporti verranno avviati al termine del video corrente.

## <a name="working-with-json-directly-advancedoptional"></a>Uso diretto di JSON (Advanced/optional)

La console multimediale supporta l'immissione di codice JSON direttamente nel prompt della console di in AltspaceVR.  JSON è il meccanismo interno con cui si abilitano le configurazioni di Media Player. Esponendo la possibilità di impostare JSON direttamente è qualcosa che consente agli utenti più avanzati di creare flussi di lavoro personalizzati in grado di soddisfare le proprie esigenze e familiarità con JSON.  Di seguito è riportata una breve descrizione della struttura JSON e dello schema in base al quale viene convalidato il JSON. Per descrizioni più dettagliate delle proprietà riportate di seguito, vedere le sezioni precedenti che comunicano sulla configurazione della console multimediale.  Questa sezione è incentrata principalmente sugli esempi di schema e sulla strutturazione per i dati JSON.

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

### <a name="media-list"></a>Elenco supporti

L'elenco dei supporti è una proprietà impostata alla radice della struttura JSON, ad esempio i ruoli e le impostazioni di riproduzione.  Si tratta di una semplice matrice che può contenere una delle seguenti strutture di configurazione multimediale. Per informazioni dettagliate su ciò che accade, vedere le descrizioni delle proprietà precedenti.

**Esempio di immagine**

*Campi obbligatori: "Name" e "imageUrl"*

```json
{
    "name": "Altspace Screenshot",
    "imageUrl": "https://pbs.twimg.com/media/CxJ-fJqUsAAFtd9.jpg",
    "skipAfter": 10
}
```

**Esempio video**

*Campi obbligatori: "Name" e "videoUrl"*

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

### <a name="schema"></a>SCHEMA

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
> Aggiornato con la console multimediale v 0.5.0