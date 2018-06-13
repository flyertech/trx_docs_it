---
title: Shopify
sidebar: mydoc_sidebar
permalink: shopify.html
folder: mydoc
---


## Panoramica
{% include_relative partials/integration_overview.md %}

## Dove inserire lo snippet trackTransaction

Dalla pagina di **Admin** del tuo Shopify, seleziona **Settings**

{% include image.html file="shopify/settings.png" url="images/shopify/settings.png" %}

Seleziona **Checkout**

{% include image.html file="shopify/checkout.png" url="images/shopify/checkout.png" %}

{% include image.html file="shopify/apikey.png" url="images/shopify/apikey.png" %}

Copia la tua API Key dalla maschera **Your API Key**. Invece di selezionare il testo puoi anche semplicemente cliccare sul tasto Copy."

Inserisci il seguente snippet nel box **Additional script**

{% include callout.html content="Nello snippet seguente dovrai sostituire \"ApiKey\" con la tua API Key che troverai sul sito di Transactionale, nella pagina **My Account -> Integration**." %}

{% include image.html file="shopify/add_script.png" url="images/shopify/add_script.png" %}

{% highlight html %}{% include_relative snippets/shopify.md %}{% endhighlight %}

Salva cliccalndo il pulsante **Save** in alto

{% include image.html file="shopify/save_settings.png" url="images/shopify/save_settings.png" %}

##  Dove inserire il loader e l'evento viewPage

Dalla pagina di **Admin** del tuo Shopify, seleziona **Online Store**

{% include image.html file="shopify/online_store.png" url="images/shopify/online_store.png" %}

Dalla pagina **Themes->current theme** clicca su **Action->Edit Code**

{% include image.html file="shopify/edit_code.png" url="images/shopify/edit_code.png" %}

{% include callout.html content="Nello snippet seguente dovrai sostituire \"ApiKey\" con la tua API Key che troverai sul sito di Transactionale, nella pagina **My Account -> Integration** come hai fatto in precedenza " %}

Clicca su **theme.liquid** e incolla lo snippet prima della chiusura del tag **<head>**

{% include image.html file="shopify/snippet.png" url="images/shopify/snippet.png" %}

{% include_relative snippets/loader_viewPage.md %}

Clicca sul pulsante **Salva** in alto 

{% include image.html file="shopify/save_edit_code.png" url="images/shopify/save_edit_code.png" %}

## Verifica integrazione e webhook
Puoi verificare il corretto funzionamento dell'integrazione tecnologica e del webhook url tramite queste semplici istruzioni:

{% include_relative partials/link_verify.md %}