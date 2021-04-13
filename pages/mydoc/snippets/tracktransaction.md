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
        // Esempio con integrazione annunci direttamente in pagina ordine
        touchpointType: 'auto', 
    }
);
</script>
```
```html
<!-- Solo per i publisher - Indica il punto in cui mostrare il banner o gli annunci -->
<div id="tr_touchpoint_container"></div>
```