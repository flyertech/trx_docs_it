---
title: Snippet nella pagina carrello
sidebar: mydoc_sidebar
permalink: mydoc_snippet_carrello.html
folder: mydoc
---

## Overview
Lo snippet deve essere implementato nella **pagina Carrello** per monitorare gli utenti che abbandonano l'ordine prima del pagamento.
Deve essere implementato nel header del codice sorgente della pagina. I **tag vengono caricati in modo asincrono**, di modo che ciò **non interferisca** con i tempi di caricamento della pagina o con l'esperienza dell'utente.
Nell'implementazione nella pagina Carrello, sarà necessario il trasferimento dinamico di ID, prezzi e quantità di ciascun prodotto aggiunto al carrello, insieme ai parametri email e relativi al tipo di sito.

## L'evento viewBasket (visualizzazione Carrello)
Tiene traccia della pagina del carrello con i dettagli del suo contenuto.
In questo caso i prodotti (items) possono essere forniti solo come oggetti, poiché ci sarà sempre almeno un attributo in più da fornire: la quantità.

```js
_trx.push({
    event: 'viewBasket',
    items: [{
        id: 'ABC123', // REQUIRED
        quantity: 1, // REQUIRED
        price: '123.23', // Strings are preferred
        name: 'Example',
        categoryId: 123,
        categoryName: 'Custom or Google category name'
    }]
});
```

[Google merchant categories](https://www.google.com/basepages/producttype/taxonomy-with-ids.en-US.txt)