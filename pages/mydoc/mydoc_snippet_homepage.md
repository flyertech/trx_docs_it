---
title: Snippet nella home page
sidebar: mydoc_sidebar
permalink: mydoc_snippet_homepage.html
folder: mydoc
---

## Panoramica
L'implementazione sulla Home page ci consente di monitorare i bouncer (ovvero gli utenti che  accedono alla Home page ma lasciano il sito senza effettuare acquisti). 

La prima parte dello snippet deve essere implementato nel header del codice sorgente di ogni pagina del sito. Il **tag si carica in modo asincrono**, e dunque **non interferirà** con il tempo di caricamento della pagina o con l'esperienza dell'utente.

Devono essere trasferiti dinamicamente solo due parametri: setAccount e setEmail.


Questo snippet va **inserito nel tag <head>**

```js
<script>
    // Initialize the event queue
    window._trx = window._trx || [];
    window._trx.push(
        { event: 'setAccount', account: 'API-KEY', country: 'IT' });
        { event: 'setEmail', email: 'TRIMMED AND LOWERCASE USER EMAIL ADDRESS', country: 'IT' });
</script>
<script src="/integration/v2/main.js" async="true"></script>
```

Questo snippet va **inserito subito dopo il tag <body>**

```js
<script>
    // Track an event
    window._trx.push({
        event: 'viewHome'
    });
</script>
```

## L'evento visualizzazione Home
L' evento **viewHome** è l'evento specifico usato quando il tag viene implementato sulla tua home page

```js
_trx.push({
  event: 'viewHome'
  // No other argument is supported
});
```

## Parametro setAccount
Contiene le informazioni per l'autenticazione, in questo caso l'**API Key**.

```js
_trx.push({ 
    event: 'setAccount',
    account: 'API_KEY', // REQUIRED
    country: 'IT', // REQUIRED
});
```

## Parametro setEmail
Contiene l'**indirizzo email** dell'utente corrente. Solitamente non è necessario è richiesto nei casi in cui desideri visualizzare annunci prima di una transazione, ad esempio dopo la registrazione.

```js
_trx.push({
  event: 'setEmail',
  email: 'email@address.com' // REQUIRED
});
```