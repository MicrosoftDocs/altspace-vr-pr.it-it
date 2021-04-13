---
title: Concessione dei ruoli internazionali
description: Informazioni sul sistema dei ruoli e delle funzionalità e istruzioni dettagliate per fornire agli utenti i ruoli nei AltspaceVR.
ms.date: 03/11/2021
ms.topic: article
keywords: Ruoli
ms.openlocfilehash: f8cd55fbd8ede6cedd199724a3e6b2413c5bc3e6
ms.sourcegitcommit: d84a6adf631ff02b106e682238f2861477caef1e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2021
ms.locfileid: "107212792"
---
# <a name="granting-world-roles"></a>Concessione dei ruoli internazionali

Altspace dispone di un sistema Roles and Capacity. Ogni persona può avere più ruoli e i relativi ruoli possono essere diversi a seconda della posizione in cui si trovano. Ogni ruolo, a sua volta, offre una o più funzionalità. Ad esempio, quando ci si trova nel proprio evento, si ricevono automaticamente i ruoli **Presenter** e **Moderator** . Con questi due ruoli è possibile avviare gli utenti indisciplinati e forse rilasciare i coriandoli. 

1. Modificare il mondo e scorrere verso il basso fino alla sezione **in VR** ([How to Manage Worlds](managing-worlds.md))

![Modifica dei ruoli nella sezione VR del mondo](images/granting-roles.png)

2. Modificare il campo **ruoli** se si desidera concedere ruoli specifici a utenti specifici solo per questo mondo. Se, ad esempio, si desidera concedere a un moderatore **Presenter**  +   e a calen **Moderator**, aggiungere quanto segue e selezionare **Salva**. Il formato è **{Role}, {username o email}** in ogni riga. Il nome utente non distingue tra maiuscole e minuscole. 

```
presenter,jimmy
moderator,jimmy
moderator,calen
```

3. Se si seleziona nuovamente **modifica** , verrà visualizzato quanto segue sopra il campo ruoli. Questo è il modo in cui si conosce l'aggiornamento nel database.

```
Presenters: jimmy
Moderators: jimmy,calen
```

* Per rendere effettive le modifiche in Altspace, è necessario reimpostare il mondo, forzando la riaggiunta di tutti. Di seguito è riportato un elenco completo dei ruoli.

4. Modificare il campo dei **ruoli contestuali** se si vuole concedere un ruolo a tutti gli utenti che si uniscono al mondo. Se, ad esempio, si desidera consentire agli utenti di volare e utilizzare il megafono in modo da poterli ascoltare a vicenda, aggiungere quanto segue:

```
pilot,megaphone_only
```

Dopo aver selezionato **Aggiorna**, reimpostare il mondo. Questa operazione avrà effetto solo su questo mondo. Se si vuole concedere i ruoli a un intero universo, modificare gli stessi campi nell'universo. 

## <a name="roles"></a>Ruoli 

* **Relatore** -capacità come essere in fase di esecuzione
* **Moderatore** -capacità come **Kick** per la manutenzione del decoro
* Responsabile della **bonifica** -possibilità di usare l'editor globale
* **Progetto pilota** : possibilità di impostare la modalità di volo e generare lo strumento 6DOF Flight
* **Megaphone_only** la possibilità di comunicare con le orecchie degli utenti ovunque si trovino nel mondo
* **Showcase_new_sdk** la possibilità di generare app MRE SDK

## <a name="troubleshooting"></a>Risoluzione dei problemi

**È possibile eliminare I ruoli?**
Non dal form in questo momento, quindi è possibile archiviare un Richiesta di supporto in help.altvr.com, che verrà preso in considerazione

**I ruoli vengono copiati quando un mondo viene importato da un altro?**
No, i ruoli non vengono copiati