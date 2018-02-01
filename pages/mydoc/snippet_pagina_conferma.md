---
title: Snippet nella pagina di conferma dell'ordine
sidebar: mydoc_sidebar
permalink: snippet_pagina_conferma.html
folder: mydoc
---

## Overview
La **pagina di conferma** dell'ordine è quella visualizzata all'utente quando avrà completato un acquisto sul sito; normalmente mostra un ID ordine e un riepilogo dell'ordine.
Lo snippet deve essere installato nella pagina di conferma dell'ordine per monitorare i prodotti acquistati dagli utenti. Il monitoraggio di ciò che viene acquistato dal cliente consente di ottimizzare la visualizzazione dei banner in modo che i prodotti già acquistati dal cliente non vengano mostrati sui banner che il cliente vedrà in futuro. Acquisire queste informazioni consentirà inoltre di misurare il ROI sui banner Transactionale.

Nell'implementare lo snippet nella pagina di Conferma dell'ordine, sarà necessario trasferire dinamicamente ID, prezzi e quantità dei prodotti acquistati dall'utente, l'ID ordine/transazione, i parametri email.

{% include_relative partials/loader_warning.md %}

## L'evento trackTransaction (monitoraggio Transazione)
Tiene traccia di una **trasazione completa** (ordine, booking etc.). Ciò consentirà il tracciamento delle conversioni oltre ad intercettare la consegna delle offerte attraverso uno dei **touchpoints** disponibili: web, mail o bulk.  Per i touchpoint Web è possibile impostare **touchpointType**: "web" e chiamerà implicitamente [triggerWebTouchpoint](#triggerWebTouchpoint).

{% include_relative snippets/tracktransaction.md %}