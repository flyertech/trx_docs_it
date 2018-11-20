---
title: Invio Sms
sidebar: mydoc_sidebar
permalink: send_sms.html
folder: mydoc
---

Puoi inviare un sms alternativamente all'email transactional, è neccessario disporre dell'apiKey, reperibile dal tuo account transactionale ed eseguire una chiamata POST come segue:
Per l'invio di Sms è necessario disporre dell'Auth Key.


{% include callout.html type="success" content="POST /api/v1/send" %}
I paramentri necessari sono:

|Parametri| Descrizione|
|-------|------|
|phone| Formato internazionale, comprensivo di prefisso senza '+'|
|sender_id| Stringa di lettere, numeri, punto e spazi (Max 11 caratteri)|
|body| Contenuto sms|
|webhook_url| Url su cui ricevere il webhook |

Se la chiamata va a buon fine otterrai una response di questo tipo che ti verrà inviata automaticamente configurando un webhook_url.

```js
Response: {
  [
    {
        "id": [
            "141342134131341"
        ],
        "from": "Transactionale",
        "to": "151514561456"
    }
]

}
```

{% include callout.html type="info" content="GET /api/v1/send/{authKey}" %}


|Parametri| Descrizione|
|-------|------|
|authKey| Api Key reperibile dal tuo account Transactionale|

{% include callout.html type="danger" content="DELETE /api/v1/send/{authKey}" %}


|Parametri| Descrizione|
|-------|------|
|authKey| Api Key reperibile dal tuo account Transactionale|