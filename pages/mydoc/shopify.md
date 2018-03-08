---
title: Shopify
sidebar: mydoc_sidebar
permalink: shopify.html
folder: mydoc
---


## Panoramica
{% include_relative partials/integration_overview.md %}

{% include callout.html content="L'integrazione semplificata è sconsigliata per l'attività di publishing in quanto riduce quantità e qualità della profilazione automatica, e quindi riduce le performance di lead generation." %}

## Dove inserire lo snippet trackTransaction

Dalla pagina di **Admin** del tuo Shopify, seleziona **Settings**

![image-title-here](images/shopify/settings.png){:class="img-responsive"}

Seleziona **Checkout**

![image-title-here](images/shopify/checkout.png){:class="img-responsive"}

{% include callout.html content="Nello snippet seguente dovrai sostituire \"ApiKey\" con la tua API Key che troverai sul sito di Transactionale, nella pagina **My Account -> Integration**." %}

![image-title-here](images/shopify/apikey.png){:class="img-responsive"}

Copia la tua API Key dalla maschera “Your API Key”. Invece di selezionare il testo puoi anche semplicemente cliccare sul tasto Copy."

\n Inserisci il seguente snippet nel box **Additional script**

![image-title-here](images/shopify/add_script.png){:class="img-responsive"}


{% highlight html %}{% include_relative snippets/shopify.md %}{% endhighlight %}



Salva cliccalndo il pulsante **Save** in alto

![image-title-here](images/shopify/save_settings.png){:class="img-responsive"}

##  Dove inserire il loader e l'evento viewPage

Dalla pagina di **Admin** del tuo Shopify, seleziona **Online Store**

![image-title-here](images/shopify/online_store.png){:class="img-responsive"}

Dalla sezione **Themes** clicca su **Action->Edit Code**

![image-title-here](images/shopify/edit_code.png){:class="img-responsive"}

{% include callout.html content="Nello snippet seguente dovrai sostituire \"ApiKey\" con la tua API Key che troverai sul sito di Transactionale, nella pagina **My Account -> Integration** come hai fatto in precedenza " %}

Clicca su **theme.liquid** e incolla lo snippet prima della chiusura del tag **<head>**

![image-title-here](images/shopify/snippet.png){:class="img-responsive"}

{% include_relative snippets/loader_viewPage.md %}

Clicca sul pulsante **Salva** in alto 

![image-title-here](images/shopify/save_edit_code.png){:class="img-responsive"}