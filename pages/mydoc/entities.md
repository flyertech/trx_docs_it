---
title: Documentazione entità
sidebar: mydoc_sidebar
permalink: entities.html
folder: mydoc
---

## Customer

```js
customer: {
    firstName: 'Nome',
    lastName: 'Cognome',
    company: 'Ragione sociale',
    email: 'indirizzo@email.it',
    birthdate: '1900-01-01', // AAAA-MM-GG
    gender: 'm', // m o f
    optin: true // Default: true - se l'utente ha accettato di ricevere comunicazioni commerciali da terzi
}
```

## Address

```js
address: {
    address: 'test',
    address2: 'test',
    city: 'Test',
    postalCode: '70121',
    country: 'IT',
    phone: '123456789',
    phoneMobile: '123456789',
},
```

## Transaction

```js
transaction: {
    id: 'ABC123', // Order number
    subtotal: 1,
    shipping: 1,
    discount: 0.5,
    total: 1.5, // Required
    coupon: 'CPN', 
    currency: 'EUR', // EUR by default
},
```

## Item (full version)

```js
item: {
    id: 'ABC123', // The internal product code
    price: '12.34',
    name: 'Pizza', 
    categoryId: 123, // Google merchant center category ID 
    categoryName: 'My category', // Custom or Google category name
    barcode: '0000123456789' // EAN or UPC
}
```
[Categorie Google Merchant](https://www.google.com/basepages/producttype/taxonomy-with-ids.it-IT.txt)
[Google Merchant categories](https://www.google.com/basepages/producttype/taxonomy-with-ids.en-US.txt)