---
title: Documentazione eventi
sidebar: mydoc_sidebar
permalink: events.html
folder: mydoc
---


## Tipi di evento

### setAccount
Contiene le informazioni per l'autenticazione.

```js
_trx.push({ 
  event: 'setAccount',
  account: 'API_KEY', // REQUIRED
  country: 'IT' // REQUIRED
});

```

### setEmail
Contiene l'indirizzo email dell'utente corrente. Solitamente non è necessario è richiesto nei casi in cui desideri visualizzare annunci prima di una transazione, ad esempio dopo la registrazione.

```js
_trx.push({
  event: 'setEmail',
  email: 'email@address.com' // REQUIRED
});

```

### viewHome
Traccia la visita della home page.

```js
_trx.push({
  event: 'viewHome'
  // No other argument is supported
});

```

### viewItem
Tiene traccia della visita sulla pagina di un singolo oggetto (ad esempio prodotto, proprietà, ecc.)
Gli articoli possono essere forniti in due modi:

- solo id, se la company ha precedentemente fornito un feed del proprio catalogo
- un oggetto che descrive tutti i dettagli necessari

```js
// Example with previously provided product feed
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
    name: 'Example', 
    categoryId: 123, // Google merchant center category ID 
    categoryName: 'My Category', // Custom or Google category name
    barcode: '0000123456789'
  }
});

```

### viewList
Traccia la visita di una lista di prodotti, catalogo o risultati di ricerca.
Gli articoli possono essere forniti in due modi:

- solo id, se la company ha precedentemente fornito un feed del proprio catalogo,
- un oggetto che descrive tutti i dettagli necessari.

```js
// Example with previously provided product feed
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
    name: 'Example', 
    categoryId: 123, // Google merchant center category ID 
    categoryName: 'Custom or Google category name'
  }]
});
```

### viewBasket
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

### trackTransaction
Tiene traccia di una transazione completa (ordine, booking etc.). Ciò consentirà il tracciamento delle conversioni oltre ad intercettare la consegna delle offerte attraverso uno dei touchpoints disponibili: web, mail o bulk.  Per i touchpoint Web è possibile impostare touchpointType: "web" e chiamerà implicitamente triggerWebTouchpoint.

{% include_relative snippets/tracktransaction.md %}

### flush
Serve per attivare manualmente l'invio di dati al server di tracciamento.

```js
window._trx.push({ event: 'flush' });
```

### setTouchpointId
Imposta il touchpoint id desiderato. Utile in caso di account per più siti o per più tipi di touchpoints (transactional, bulk o web).

```js
window._trx.push({ event: 'setTouchpointId', touchpointId: 1 });
```

### triggerWebTouchpoint
Attiva la visualizzazione delle offerte all'interno della pagina web. Richiede un `<div>` sulla pagina con id "tr_touchpoint_container". L'ID può essere personalizzato passando un argomento containerId nell'evento.

```js
window._trx.push(
    { event: 'setAccount', account: '123', country: 'IT'},
    { event: 'trackTransaction', [...] },
    { 
        event: 'triggerWebTouchpoint',
        touchpointId: 1, // REQUIRED: set here or before with a setTouchpointId event
        containerId: 'tr_touchpoint_container' // OPTIONAL, this is the default
    }
);
```

### triggerMailTouchpoint
Richiede l'invio di una mail promozionale verso l'utente fornito senza legarla ad una transazione.

```js
    window._trx.push(
      { event: 'setAccount', account: '123', country: 'IT'},
      { 
        event: 'triggerMailTouchpoint',
        touchpointId: 1, // set here or before with a setTouchpointId event
        customer: {
            firstName: 'Nome',
            lastName: 'Cognome',
            company: 'Ragione sociale',
            email: 'email@address.com',
            birthdate: '1900-01-01', // YYYY-MM-DD or YYYY only
            gender: 'm', // m o f
            optin: true // Default: true - se l'utente ha dato il consenso per ricevere comunicazioni commerciali da terzi
        },
      }
    );
```

### viewPage
Traccia una visita ad una pagina generica. Ad esempio vuoi generare un nuovo lead quando un utente vede la pagina www.yoursite.com/success.
{% include_relative snippets/viewpage.md %}

Nel settings della campagna inserirai www.yoursite.com/success come url finale del funnel.

### customEvent
Traccia uno specifico evento. 
Può essere usato per i funnels in Sigle Page Application o dovunque per tracciare un evento dopo il caricamento della pagina.

```js
    window._trx.push(
      { event: 'setAccount', account: '123', country: 'IT'},
      { event: 'customEvent', name: 'my-custom-event-name'}
    );
```
Per catturare l'evento devi configurare la campagna inserendo il nome dell'evento nel campo dedicato.

