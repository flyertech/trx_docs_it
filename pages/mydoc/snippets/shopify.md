{% raw %}
<script>
    window._trx = window._trx || [];
    window._trx.push({
        event: 'setAccount', account: '*** LA TUA AUTH KEY ***', country: '*** IL TUO CODICE NAZIONE A 2 LETTERE ISO (ad es. IT) ***'
    });
</script>
<script src="https://static.transactionale.com/trx/v2/trx.js" async="true"></script>
<script>
    window._trx.push(
        {
            'event' : 'trackTransaction',
            'transaction':{
                'id': "{{order.order_number}}",
                'subtotal': "{{order.subtotal_price | money_without_currency}}",
                'shipping': "{{order.shipping_price | money_without_currency}}",
                'discount': "{% for discount in order.discounts %} {{discount.total_amount | money_without_currency}}{% endfor %}" ,
                'total': "{{order.total_price | money_without_currency}}",
                'coupon': "{% for discount in order.discounts %} {{discount.code}} {% endfor %}" ,
                'currency': "{{shop.currency}}",
            },
            'items': [
                {% for line_item in order.line_items %}
                {
                    'id': "{{line_item.product.id}}",
                    'price': "{{line_item.product.price | money_without_currency}}",
                    'quantity': "{{line_item.quantity}}"
                },
                {% endfor %} ],
            'address':{
                'address': "{{order.billing_address.address1}}",
                'address2': "{{order.billing_address.address2}}",
                'city': "{{order.billing_address.city}}",
                'postalCode': "{{order.billing_address.zip}}",
                'country': "{{order.billing_address.country_code}}",
                'phone': "{{order.billing_address.phone}}",
            },
            'customer': {
                'firstName': "{{order.customer.first_name}}",
                'lastName': "{{order.customer.last_name}}",
                'company': "{{order.customer_address.company}}",
                'email': "{{order.customer.email}}",
                'optin' : "{{checkout.buyer_accepts_marketing}}",
            },
            "touchpointType": "auto"
        });
</script>
<div id="tr_touchpoint_container"></div>
{% endraw %}