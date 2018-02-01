---
title: Eventi personalizzati
sidebar: mydoc_sidebar
permalink: custom_events.html
folder: mydoc
---

Gli eventi personalizzati consentono di creare funnel personalizzati di generazione dei lead.
Ad esempio, tramite l'evento [viewPage](#viewPage) è possibile generare un lead solo quando l'utente, una volta cliccata l'offerta, visualizza una determinata pagina.
L'evento [customEvent](#customEvent) consente di generare un lead solo quando viene triggerato l'evento specificato, ad es. l'utente compila un form, o vince un quiz. E' utile nel caso di One Page Applications, in cui non c'è refresh della pagina.

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
    { event: 'viewPage'}
);
</script>
```
Nel settings della campagna selezionerai *URL* come *Lead funnel type* inserirai www.yoursite.com/success come url.

## customEvent
Permette di tracciare un generico evento da definito.
Può essere usato per i funnels in Single Page Application o dovunque per tracciare un evento dopo il caricamento della pagina.

```js
window._trx.push(
    { event: 'customEvent', name: 'my-custom-event-name'}
);
```
Per catturare l'evento devi configurare la campagna inserendo il nome dell'evento nel campo dedicato, dopo aver selezionato *Event* nel campo *Lead funnel type*.