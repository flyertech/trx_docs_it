---
title: Snippet nella pagina di Risultati della ricerca/Catalogo
sidebar: mydoc_sidebar
permalink: mydoc_snippet_pagina_ricerca.html
folder: mydoc
---

## Panoramica
Una **pagina risultati della ricerca** mostra più prodotti, può trattarsi di una pagina relativa a una categoria oppure di una pagina con i risultati della ricerca. L'implementazione dello snippet in queste pagine ci consente  di monitorare l'**interesse dell'utente per determinati tipi di prodotti** (ad es. i prodotti di una particolare categoria).

Molti utenti si limitano a navigare nelle pagine Categoria e Risultati della ricerca, senza fare clic per andare alle pagine specifiche dei prodotti, e dunque l'implementazione in queste pagine è la chiave per monitorare il comportamento di questi utenti.

Devi implementare lo snippet nell'intestazione di tutte le pagine del sito. Il **tag si carica in modo asincrono**, dunque **non interferirà** con il tempo di caricamento della pagina o con l'esperienza dell'utente.

Gli articoli possono essere forniti in due modi:

- solo id, se la company ha precedentemente fornito un feed del proprio catalogo,
- un oggetto che descrive tutti i dettagli necessari

## L'evento viewList (Visualizzazione elenco)

L'evento **viewList** (visualizzazione elenco) è l'evento specifico usato quando il tag viene implementato in una pagina di Risultati della ricerca o in una pagina di Elenco categorie. Gli ID dei tre principali prodotti visualizzati all'utente nella pagina devono essere trasferiti utilizzando il parametro dell'elemento in questione.

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
    id: 1, 
    price: 12.34, 
    name: 'Pizza', 
    categoryId: 123, // Google merchant center category ID 
    categoryName: 'Bontà' // Custom or Google category name
  }]
});
```


 [Google merchant categories](https://www.google.com/basepages/producttype/taxonomy-with-ids.en-US.txt)