```html
<script>
window._trx.push(
    {
        event: 'trackTransaction',
        transaction: {
            id: 'xxxxx', // Codice ordine
            total: xxx.xx, // Required
            currency: 'EUR' // EUR by default
        },
        // E' possibile omettere interamente l'oggetto customer se il sito non dispone di un opt-in dedicato alla cessione del dato a terzi
        customer: {
            firstName: 'nome', // Facoltativo
            lastName: 'cognome', // Facoltativo
            email: 'indirizzo@email.com', // Facoltativo
            optin: false // Facoltativo - se false i dati passati verranno scartati
        },
        // touchpointId: 123, // Mostra sempre il touchpoint indicato
        touchpointType: 'auto' // auto, web, mail
    }
);
</script>
```
```html
<!-- Solo per i publisher - Indica il punto in cui mostrare il banner o gli annunci -->
<div id="tr_touchpoint_container"></div>
```