---
title: Snippet nella pagina di conferma dell'ordine
sidebar: mydoc_sidebar
permalink: mydoc_snippet_pagina_conferma.html
folder: mydoc
---

## Overview
La **pagina di conferma** dell'ordine è quella visualizzata all'utente quando avrà completato un acquisto sul sito; normalmente mostra un ID ordine e un riepilogo dell'ordine.
Lo snippet deve essere installato nella pagina di conferma dell'ordine per monitorare i prodotti acquistati dagli utenti. Il monitoraggio di ciò che viene acquistato dal cliente consente di ottimizzare la visualizzazione dei banner in modo che i prodotti già acquistati dal cliente non vengano mostrati sui banner che il cliente vedrà in futuro. Acquisire queste informazioni consentirà inoltre di misurare il ROI sui banner Transactionale.

Lo snippet deve essere implementato nel header del codice sorgente di tutte le pagine del sito. Il **tag si carica in modo asincrono**, dunque **non interferirà** con il tempo di caricamento della pagina o con l'esperienza dell'utente.

Nell'implementare lo snippet nella pagina di Conferma dell'ordine, sarà necessario trasferire dinamicamente ID, prezzi e quantità dei prodotti acquistati dall'utente, l'ID ordine/transazione, i parametri email.

## L'evento trackTransaction (monitoraggio Transazione)
Tiene traccia di una **trasazione completa** (ordine, booking etc.). Ciò consentirà il tracciamento delle conversioni oltre ad intercettare la consegna delle offerte attraverso uno dei **touchpoints** disponibili: web, mail o bulk.  Per i touchpoint Web è possibile impostare **touchpointType**: "web" e chiamerà implicitamente [triggerWebTouchpoint](#triggerWebTouchpoint).


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
});
```
## L'evento flush
Serve per **attivare manualmente** l'invio di dati al server di tracciamento.
```js
window._trx.push({ event: 'flush' });
```

## L'evento setTouchpointId
Imposta il touchpoint id desiderato. Utile in caso di account per più siti o per più tipi di touchpoints (transactional, bulk o web).
```js
window._trx.push({ event: 'trackTransaction', touchpointId: 1 });
```

## L'evento triggerWebTouchpoint {#triggerWebTouchpoint}
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