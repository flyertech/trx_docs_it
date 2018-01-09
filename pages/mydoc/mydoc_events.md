---
title: Events
sidebar: mydoc_sidebar
permalink: mydoc_events.html
folder: mydoc
---


## Tipi di evento

### setAccount
Contiene le informazioni per l'autenticazione.

```js
_trx.push({ 
  event: 'setAccount',
  account: 'API_KEY', // REQUIRED
  country: 'IT', // REQUIRED
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
    id: 1, 
    price: 12.34, 
    name: 'Pizza', 
    categoryId: 123, // Google merchant center category ID 
    categoryName: 'Bontà', // Custom or Google category name
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
    name: 'Pizza', 
    categoryId: 123, // Google merchant center category ID 
    categoryName: 'Bontà' // Custom or Google category name
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
Tiene traccia di una trasazione completa (ordine, booking etc.). Ciò consentirà il tracciamento delle conversioni oltre ad intercettare la consegna delle offerte attraverso uno dei touchpoints disponibili: web, mail o bulk.  Per i touchpoint Web è possibile impostare touchpointType: "web" e chiamerà implicitamente triggerWebTouchpoint.

```js
window._trx.push(
    {
        event: 'trackTransaction',
        transaction: {
            id: 'ABC123', // Order number
            subtotal: 1,
            shipping: 1,
            discount: 0.5,
            total: 1.5, // Required
            coupon: 'CPN', 
            currency: 'EUR', // EUR by default
        },
        items: [
            {id: 1, price: 12.34, quantity: 1}, // Same format as viewBasket
            {id: 2, price: 23.45, quantity: 2},
        ],
        address: {
            address: 'test',
            address2: 'test',
            city: 'Test',
            postalCode: '70121',
            country: 'IT',
            phone: '123456789',
            phoneMobile: '123456789',
        },
        customer: {
            firstName: 'Ugo',
            lastName: 'Fantozzi',
            company: 'Megaditta',
            email: 'ugo@fantozzo.it',
            birthdate: '1983-03-06', // YYYY-MM-DD or YYYY only
            gender: 'm',
            optin: true // Default to true
        },
        // Example with web touchpoint usage
        touchpointType: 'web',
        touchpointId: '123' // REQUIRED or set before with a setTouchpointId event
        containerId: 'test' // OPTIONAL
    }
);

```

### flush
Serve per attivare manualmente l'invio di dati al server di tracciamento.
```js
window._trx.push({ event: 'flush' });

```

### setTouchpointId
Imposta il touchpoint id desiderato. Utile in caso di account per più siti o per più tipi di touchpoints (transactional, bulk o web).
```js
window._trx.push({ event: 'trackTransaction', touchpointId: 1 });

```

### triggerWebTouchpoint
Attiva la visualizzazione delle offerte (inline in the base??). Richiede un div sulla pagina con id "tr_touchpoint_container". L'ID può essere personalizzato passando un argomento containerId con l'evento.
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

### viewPage
Traccia una generica pagina. Ad esempio vuoi generare un nuovo lead quando un utente vede la pagina www.yoursite.com/success .

```html
<!-- www.yoursite.com/success -->
...
<body>
    <h1>Success!</h1>
</body>

<script>
window._trx.push(
    { event: 'setAccount', account: '123', country: 'IT'},
    { event: 'pageView'},
);
</script>
```

Nel settings della campagna inserirai www.yoursite.com/success come url finale del funnel.

### customEvent
Traccia uno specifico evento. 
Può essere usato per i funnels in Sigle Page Application o dovunque per tracciare un evento dopo il caricamento della pagina.

```js
    window._trx.push(
      { event: 'setAccount', account: '123', country: 'IT'},
      { event: 'customEvent', name: 'my-custom-event-name'},
    );
    
```
Per catturare l'evento devi configurare la campagna inserendo il nome dell'evento nel campo dedicato.

