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