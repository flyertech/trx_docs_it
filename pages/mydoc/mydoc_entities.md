---
title: Entities
sidebar: mydoc_sidebar
permalink: mydoc_entities.html
folder: mydoc
---

## Customer

```js
customer: {
    firstName: 'Ugo',
    lastName: 'Fantozzi',
    company: 'Megaditta',
    email: 'ugo@fantozzo.it',
    birthdate: '1983-03-06', // YYYY-MM-DD or YYYY only
    gender: 'm',
    optin: true // Default to true
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
    id: 1, 
    price: 12.34, 
    name: 'Pizza', 
    categoryId: 123, // Google merchant center category ID 
    categoryName: 'Bontà', // Custom or Google category name
    barcode: '0000123456789' // EAN or UPC
}
```

 [Google merchant categories](https://www.google.com/basepages/producttype/taxonomy-with-ids.en-US.txt)