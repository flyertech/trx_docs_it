---
title: Custom Events
sidebar: mydoc_sidebar
permalink: mydoc_custom_events.html
folder: mydoc
---

## viewPage
Permette di tracciare una pagina generica da te definita. Ad esempio se vuoi generare un nuovo lead quando un utente vede la pagina www.yoursite.com/success .

```html
<!-- www.yoursite.com/success -->
...
<body>
    <h1>Success!</h1>
</body>
<script>
window._trx.push(
    { event: 'setAccount', account: '123', country: 'IT'},
    { event: 'pageView'},
);
</script>
```
Nel settings della campagna inserirai www.yoursite.com/success come url finale del funnel.

## customEvent
Permette di tracciare un generico evento da definito.
Può essere usato per i funnels in Single Page Application o dovunque per tracciare un evento dopo il caricamento della pagina.

```js
window._trx.push(
    { event: 'setAccount', account: '123', country: 'IT'},
    { event: 'customEvent', name: 'my-custom-event-name'},
);
```
Per catturare l'evento devi configurare la campagna inserendo il nome dell'evento nel campo dedicato.