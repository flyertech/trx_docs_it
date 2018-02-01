---
title: Integrazione semplificata
sidebar: mydoc_sidebar
permalink: simplified_integration.html
folder: mydoc
---

## Panoramica
{% include_relative partials/integration_overview.md %}

{% include callout.html content="L'itegrazione semplificata è sconsigliata per l'attività di publishing in quanto riduce quantità e qualità della profilazione automatica, e quindi riduce le performance di lead generation." %}

## Inserisci il loader in tutte le pagine
Il tag va inserito nella sezione `<head>` della pagina.
{% include_relative snippets/loader.md %}

## Inserisci il tag `viewPage` in tutte le pagine
Questo tag può essere inserito preferibilmente prima del tag di chiusura `</body>`, oppure dopo il loader nel tag `<head>`.
{% include_relative snippets/viewpage.md %}

Puoi anche invocare l'evento `viewPage` contestualmente alla creazione del loader:
```html
<script>
    window._trx = window._trx || [];
    window._trx.push(
        { event: 'setAccount', account: '**API-KEY**', country: 'IT' },
        { event: 'viewPage' }
    );
</script>
<script src="https://static.transactionale.com/trx/v2/trx.js" async="true"></script>
```

## Inserisci il tag `trackTransaction` nella pagina di conferma ordine
Puoi inserire questo tag preferibilmente prima del tag di chiusura `</body>`, oppure dopo il loader nel tag `<head>`.
Dovrai riempire tutti i campi disponibili con i valori effettivi relativi all'ordine appena concluso.

{% include_relative snippets/tracktransaction.md %}




