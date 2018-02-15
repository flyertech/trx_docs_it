---
title: Integrazione semplificata
sidebar: mydoc_sidebar
permalink: simplified_integration.html
folder: mydoc
---

## Panoramica
{% include_relative partials/integration_overview.md %}

{% include callout.html content="L'itegrazione semplificata è sconsigliata per l'attività di publishing in quanto riduce quantità e qualità della profilazione automatica, e quindi riduce le performance di lead generation." %}

## Inserisci il tag in tutte le pagine
Il tag va inserito idealmente prima del tag di chiusura `</body>`.
Il tag include il loader, più l'evento `viewPage`:

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
Puoi inserire questo prima del tag di chiusura `</body>`, e in ogni caso prima del loader, cioè lo snippet che va inserito in ogni pagina mostrato nel paragrafo precedente.
Dovrai riempire tutti i campi disponibili con i valori effettivi relativi all'ordine appena concluso.

{% include_relative snippets/tracktransaction.md %}




