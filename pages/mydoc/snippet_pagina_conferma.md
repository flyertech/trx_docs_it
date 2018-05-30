---
title: Snippet nella pagina di conferma dell'ordine
sidebar: mydoc_sidebar
permalink: snippet_pagina_conferma.html
folder: mydoc
---

## L'evento trackTransaction (monitoraggio Transazioni)
Lo snippet deve essere installato nella pagina di conferma dell'ordine per monitorare i prodotti acquistati dagli utenti. 
Nell'implementare lo snippet nella pagina di Conferma dell'ordine, sarà necessario trasferire dinamicamente ID, prezzi e quantità dei prodotti acquistati dall'utente, l'ID ordine/transazione, i parametri email.

{% include_relative partials/loader_warning.md %}

Tiene traccia di una **trasazione completa** (ordine, booking etc.). Ciò consentirà il tracciamento delle conversioni oltre ad intercettare la consegna delle offerte attraverso uno dei **touchpoints** disponibili: web, mail o bulk.  Per i touchpoint Web è possibile impostare **touchpointType**: "web" e chiamerà implicitamente [triggerWebTouchpoint](#triggerWebTouchpoint).



{% include_relative snippets/tracktransaction.md %}

{% include_relative partials/google_categories.md %}

## Touchpoint web o auto
Se utilizzi il touchpoint web dovrai specificare dove vuoi che vengano mostrate le offerte nella tua pagina perciò dovrai inserire un `<div id="tr_touchpoint_container"></div>` nel punto desiderato. 

## Banner offerte
Nel caso si utilizzi un touchpoint web in versione banner, è possibile scegliere due layout: orizzontale (default) oppure verticale.

{% include image.html file="banner_horizontal" url="images/banner_horizontal.png" %}

Aggiungendo la classe `tr-touchpoint-layout-vertical` nel `<div>` in questo modo:<br>
 `<div id="tr_touchpoint_container" class="tr-touchpoint-layout-vertical"></div>` <br>
 il banner avrà layout verticale:

{% include image.html file="banner_vertical" url="images/banner_vertical.png" %}


