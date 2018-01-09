---
title: Payload keys mapping
sidebar: mydoc_sidebar
permalink: mydoc_payload.html
folder: mydoc
---

## Overwiev


### Payload keys mapping

```js
payloadKeysMapping = {
    version: 'vv',
    email: 'ue',
    event: 'ev',
    customEventName: 'en',
    touchpointId: 'ut',
    touchpointType: 'uy',
    isTransaConversion: 'ec',
    user: {
        'res': 'ur',
        'ua': 'ua',
        'lang': 'ul'
    },
    page: {
        'href': 'ph',
        'lang': 'pl',
        'title': 'pt',
        'charset': 'pc',
        'keywords': 'pk',
        'description': 'pd'
    },
    transaction: {
        'id': 'ti',
        'subtotal': 'ts',
        'shipping': 'th',
        'discount': 'td',
        'coupon': 'tc',
        'total': 'tt',
        'currency': 'tv'
    },
    itemIDs: 'ji', // No sub-fields, so one-level key only
    items: {
        'id': 'ii',
        'price': 'ip',
        'quantity': 'iq',
        'name': 'in',
        'categoryId': 'ic',
        'categoryName': 'id',
        'barcode': 'ib' // EAN or UPC
    },
    address: {
        'firstName': 'af',
        'lastName': 'al',
        'company': 'ac',
        'address': 'aa',
        'address2': 'ab',
        'city': 'at',
        'postalCode': 'az',
        'country': 'an',
        'phone': 'ap',
        'phoneMobile': 'am'
    },
    customer: {
        'firstName': 'cf',
        'lastName': 'cl',
        'company': 'cc',
        'birthdate': 'cb',
        'gender': 'cg',
        'optin': 'co'
    }
}
```