---
title: Invio di SMS singoli
sidebar: mydoc_sidebar
permalink: send_sms.html
folder: mydoc
---

E' possibile utilizzare le API di Transactionale per inviare SMS a destinatari singoli.

# Autenticazione

Per autenticarsi è necessario utilizzare l'API KEY reperibile dal tuo account Transactionale, passandola come valore dell'header Authorization.

Esempio:

```js
GET https://api.transactionale.com/platform/api/sms/send
Authorization: <API KEY>
```
Esempio cURL:
```sh
curl -H "Authorization: abc123" "https://api.transactionale.com/platform/api/sms/send"
```
# Invio di un SMS

{% include callout.html type="success" content="POST /platform/api/sms/send" %}

Esempio di chiamata:

```js
POST https://api.transactionale.com/platform/api/sms/send
Authorization: <API KEY>
Content-Type: application/json
BODY:
{
    "phone": "393000000000",
    "sender_id": "MyShop",
    "body": "Hello, world!",
    "webhook_url": "https://www.myshop.com/webhook/sms"
}
```
Esempio cURL:
```sh
curl -H "Authorization: abc123" \
-H "Content-Type: application/json" \
-X POST -d '{"phone": "393000000000", "sender_id": "MyShop", "body": "Hello, world!", "webhook_url": "https://www.myshop.com/webhook/sms"}' \
"https://api.transactionale.com/platform/api/sms/send"
```

## Descrizione dei parametri

|Parametri| Descrizione|
|-------|------|
|phone| (string) Formato internazionale (MSISDN), comprensivo di prefisso senza '+'|
|sender_id| (string) Stringa di lettere, numeri, punto e spazi (Max 11 caratteri)|
|body| (string) Contenuto dell'SMS|
|webhook_url| (string) *(Opzionale)* Url su cui ricevere la chiamata per il webhook |

Se la chiamata va a buon fine otterrai una risposta di questo tipo:

```js
HTTP STATUS: 201 CREATED
{
    "id": 123,
    "phone": "39300000000",
    "sender_id": "MyShop",
    "body": "Il mio SMS!",
    "status": "pending",
    "delivery_status": "unknown",
    "country": "IT",
    "is_two_way": false,
    "webhook_url": "https://www.myshop.com/webhook/sms",
    "url": "https://api.transactionale.com/platform/api/sms/send/123",
}
```

## Descrizione della risposta

|Parametri| Descrizione|
|-------|------|
|id| (integer) |
|phone| (string) Formato internazionale (MSISDN), comprensivo di prefisso e senza +|
|sender_id| (string) Stringa di lettere, numeri, punto e spazi (Max 11 caratteri)|
|body| (string) Contenuto dell'SMS|
|status| (string) *sent* o *pending*|
|delivery_status| (string) *delivered*, *failed*, *unknown*|
|url| (string) URL API di questo SMS|
|webhook_url| (string) L'URL a cui verranno inviate le notifiche di consegna (webhook)|
|country| (string) 'AF' or 'AL' or 'AG' or 'AR' or 'AU' or 'AT' or 'BY' or 'BE' or 'BA' or 'BR' or 'BG' or 'KH' or 'CA' or 'CL' or 'CN' or 'CO' or 'HR' or 'CU' or 'CY' or 'CZ' or 'KP' or 'DK' or 'DO' or 'EG' or 'ER' or 'EE' or 'FI' or 'FR' or 'GF' or 'DE' or 'GI' or 'GR' or 'GP' or 'HK' or 'HU' or 'IS' or 'IE' or 'IL' or 'IT' or 'JP' or 'JO' or 'KR' or 'LI' or 'LU' or 'MO' or 'MT' or 'MQ' or 'MC' or 'ME' or 'NA' or 'NL' or 'NZ' or 'NO' or 'PA' or 'PE' or 'PH' or 'PL' or 'PT' or 'RO' or 'RU' or 'SM' or 'SA' or 'RS' or 'SK' or 'SL' or 'ZA' or 'ES' or 'SE' or 'CH' or 'TW' or 'MK' or 'TN' or 'TR' or 'TC' or 'UG' or 'UA' or 'GB' or 'US' or 'UY' or 'VE' or 'YE'|
|is_two_way| (bool) Se questo SMS prevede la possibilità di ricevere risposte (non supportato)|

Esempio di riposta di errore:
```js
HTTP STATUS: 400 BAD REQUEST
{
    "errors": {
        "phone": [
            "Number is too long"
        ],
        "sender_id": [
            "Sender ID is longer than 11 chars.",
            "Sender ID contains invalid chars: +"
        ]
    }
}
```
# Lettura dello stato di un SMS

{% include callout.html type="info" content="GET /api/v1/send/\<id\>" %}

Risposta:
```js
HTTP STATUS: 200 OK
{
    "id": 123,
    "phone": "39300000000",
    "sender_id": "MyShop",
    "body": "Il mio SMS!",
    "status": "pending",
    "delivery_status": "unknown",
    "country": "IT",
    "is_two_way": false,
    "webhook_url": "https://www.myshop.com/webhook/sms",
    "url": "https://api.transactionale.com/platform/api/sms/send/123",
}
```

# Ricezione delle notifiche di consegna (webhook)

TODO