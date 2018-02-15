---
title: Snippet nella pagina carrello
sidebar: mydoc_sidebar
permalink: snippet_carrello.html
folder: mydoc
---

## L'evento viewBasket (visualizzazione Carrello)
Lo snippet tiene traccia della pagina del carrello con i dettagli del suo contenuto.
Deve essere implementato nella **pagina Carrello** per monitorare gli utenti che abbandonano l'ordine prima del pagamento.

{% include_relative partials/loader_warning.md %}

In questo caso i prodotti (items) possono essere forniti solo come oggetti, poiché ci sarà sempre almeno un attributo in più da fornire: la quantità.

```js
_trx.push({
    event: 'viewBasket',
    items: [{
        id: 'ABC123', // OBBLIGATORIO
        quantity: 1, // OBBLIGATORIO
        price: '123.23', // Il formato stringa è preferibile
        name: 'Example',
        categoryId: 123, // Google category ID
        categoryName: 'Nome categoria custom o nome categoria Google'
    }]
});
```

[Google merchant categories (versione ITA)](https://www.google.com/basepages/producttype/taxonomy-with-ids.it-IT.txt)
[Google merchant categories (versione USA)](https://www.google.com/basepages/producttype/taxonomy-with-ids.en-US.txt)
