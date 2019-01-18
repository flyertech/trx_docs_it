---
title: Banner in email
sidebar: mydoc_sidebar
permalink: banner_email.html
folder: mydoc
---

### Inviare offerte nelle proprie email
Per i **publisher abilitati**, è possibile **inserire nelle mail inviate un banner** contenente un’offerta selezionata automaticamente da Transactionale, per incrementare il numero di offerte veicolate e le possibilità di monetizzazione e fidelizzazione.

### Caratteristiche principali
Il banner email non prevede la trasmissione di dati personali a Transactionale, ed è quindi **conforme al GDPR** senza necessità di intervenire su consensi e privacy policy.
L’**integrazione è immediata** in quanto consiste nell’inserimento di una semplice immagine con un link nel template delle email inviate.

### Attivazione del touchpoint
Dalla sezione **Monetize -> Web Touchpoints** del tuo account Transactionale, aggiungi un nuovo touchpoint con formato **Email Banner**:

{% include image.html file="email_banner.png" url="images/email_banner.png" %}

Si aprirà un box di dettaglio con dentro due URL:

{% include image.html file="email_banner2.png" url="images/email_banner2.png" %}

E’ possibile utilizzare questi due URL per generare il tag immagine a mano, oppure cliccando sul pulsante Snippet è disponibile un tag di esempio già pronto da incollare.

{% include callout.html content="IMPORTANTE: è necessario **personalizzare gli URL** prima dell’utilizzo" %}

### Personalizzazione degli URL
Per assicurare il corretto funzionamento del touchpoint, è necessario sostituire la parte **{transaction_id}** dei due URL con una variabile univoca per ogni mail inviata, ad esempio il numero d’ordine. Verificare nella documentazione della propria piattaforma come utilizzare le variabili.
Esempio:
```html
https://trto.it/m/xxxxxx/yyy/b?transaction_id={ $order->id }
```

Se si desidera inserire il banner in più tipi di email con lo stesso transaction_id, è consigliabile utilizzare un prefisso per distinguere i contenuti, ad es:
```html
https://trto.it/m/xxxxxx/yyy/b?transaction_id=order_confirmation_{ $order->id }
```

{% include callout.html content="IMPORTANTE: il valore del campo **transaction_id** deve essere identico in entrambi gli URL!" %}


### Posizionamento del banner
E’ possibile **inserire il banner in qualsiasi punto della mail**, garantendo che possa occupare il 100% della larghezza del layout, ad es. inserendo l’**apposito stile nel tag**:

```html
<a href="https://trto.it/m/xxxxxx/yyy/click?transaction_id={transaction_id}" target="_blank">
  <img src="https://trto.it/m/xxxxxx/yyy/b?transaction_id={transaction_id}" style="width: 100%">
</a>
```
