```js
window._trx.push(
    {
        event: 'trackTransaction',
        transaction: {
            id: 'ABC123', // Codice ordine
            subtotal: 123.45,
            shipping: 3.5,
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
            firstName: 'Nome',
            lastName: 'Cognome',
            company: 'Ragione sociale',
            email: 'indirizzo@email.it',
            birthdate: '1900-01-01', // AAAA-MM-GG
            gender: 'm', // m o f
            optin: true // Se l'utente ha dato il consenso per le comunicazioni commerciali
        },
        // Esempio con integrazione annunci direttamente in pagina ordine
        touchpointType: 'web', // Default: mail
        touchpointId: '123', // OBBLIGATORIO se touchpointType = 'web'
        containerId: 'test' // Default: tr_touchpoint_id - il <div> dentro cui mostrare le offerte
    }
);
```