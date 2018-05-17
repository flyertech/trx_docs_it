```js
window._trx.push(
    {
        event: 'trackTransaction',
        transaction: {
            id: 'xxxxx', // Codice ordine
            subtotal: xxx.xx,
            shipping: xxx.xx,
            discount: xxx.xx,
            total: xxx.xx, // Required
            coupon: 'xxx', 
            currency: 'EUR', // EUR by default
        },
        items: [
            {id: x, price: xx.xx, quantity: x}, 
            {id: x, price: xx.xx, quantity: x},
        ],
        address: {
            address: 'xxxxxx',
            address2: 'xxxxxx',
            city: 'xxxxx',
            postalCode: 'xxxxx',
            country: 'IT',
            phone: 'xxxxxxxx',
            phoneMobile: 'xxxxxxxxx',
        },
        customer: {
            firstName: 'Xxxxx',
            lastName: 'Xxxxxxx',
            company: 'xxxxxxxx',
            email: 'xxxxx@xxxx.xx',
            birthDate: 'aaaa-mm-gg',
            gender: 'x', 
            optin: xxxx // Se l'utente ha dato il consenso per le comunicazioni commerciali
        },
        // Esempio con integrazione annunci direttamente in pagina ordine
        touchpointType: 'auto', 
    }
);
```
```html
<div id="tr_touchpoint_container"></div>
```