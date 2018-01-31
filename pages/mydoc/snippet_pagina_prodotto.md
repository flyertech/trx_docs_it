---
title: Snippet nella pagina prodotto
sidebar: mydoc_sidebar
permalink: snippet_pagina_prodotto.html
folder: mydoc
---

## Overview
Una **pagina Prodotto** contiene i dettagli relativi ad un prodotto specifico. L'implementazione nelle pagine Prodotto rappresenta l'elemento fondamentale del processo di monitoraggio, poiché è proprio in queste pagine che l'intento dell'utente viene espresso in modo più compiuto. Vi sono molti utenti che accedono direttamente alle pagine relative ai prodotti senza essere passati per le pagine contenenti i risultati ricerca (o di listing).

{% include_relative partials/laoder_warning.md %}

## L'evento viewItem (visualizzazione elemento)
Tiene traccia della visita sulla pagina di un singolo oggetto (ad esempio prodotto, proprietà, ecc.)
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

[Google merchant categories](https://www.google.com/basepages/producttype/taxonomy-with-ids.it-IT.txt)
[Google merchant categories](https://www.google.com/basepages/producttype/taxonomy-with-ids.en-US.txt)