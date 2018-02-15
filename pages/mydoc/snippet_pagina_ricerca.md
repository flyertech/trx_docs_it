---
title: Snippet nella pagina di Risultati della ricerca/Catalogo
sidebar: mydoc_sidebar
permalink: snippet_pagina_ricerca.html
folder: mydoc
---

## L'evento viewList (Visualizzazione elenco)
L'evento **viewList** (visualizzazione elenco) è l'evento specifico usato quando il tag viene implementato in una pagina di Risultati della ricerca o in una pagina di Elenco categorie.

Gli articoli possono essere forniti in due modi:

- solo id, se la company ha precedentemente fornito un feed del proprio catalogo,
- un oggetto che descrive tutti i dettagli necessari

Generalmente è sufficiente tracciare i primi 3 prodotti.

{% include_relative partials/loader_warning.md %}

Gli ID dei prodotti nello snippet devono essere esattamente gli stessi di quelli del data feed del proprio prodotto.

```js
_trx.push({
  event: 'viewList',
  itemIDs: ['ABC123', 'ABC124']
});

// Example of full product specification
_trx.push({
  event: 'viewList',
  items: [{
        id: 'ABC123', 
        price: '12.34', 
        name: 'Product name', 
        categoryId: 123, // Google merchant center category ID 
        categoryName: 'My Category', // Custom or Google category name
        barcode: '0000123456789'
      }]
});
```

{% include_relative partials/google_categories.md %}