---
title: Snippet nella pagina prodotto
sidebar: mydoc_sidebar
permalink: snippet_pagina_prodotto.html
folder: mydoc
---

## L'evento viewItem (visualizzazione elemento)

Tiene traccia della visita sulla pagina di un singolo oggetto (ad esempio prodotto, proprietà, ecc.)

{% include_relative partials/loader_warning.md %}

Gli articoli possono essere forniti in due modi:

- solo id, se la company ha precedentemente fornito un feed del proprio catalogo,
- un oggetto che descrive tutti i dettagli necessari.

```js
    _trx.push({
      event: 'viewItem',
      itemID: 'ABC123'
    });
    
    // Example of full product specification
    _trx.push({
      event: 'viewItem',
      item: {
        id: 'ABC123', 
        price: '12.34', 
        name: 'Product name', 
        categoryId: 123, // Google merchant center category ID 
        categoryName: 'My Category', // Custom or Google category name
        barcode: '0000123456789'
      }
    });
```

{% include_relative partials/google_categories.md %}