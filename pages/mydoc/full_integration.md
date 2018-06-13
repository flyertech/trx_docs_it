---
title: Integrazione completa
sidebar: mydoc_sidebar
permalink: full_integration.html
folder: mydoc
---

### Panoramica
{% include_relative partials/integration_overview.md %}

### Dove dovresti implementare lo snippet
Per prima cosa, bisogna inserire il loader [come descritto qui.](snippet_loader.html) 
Successivamente, devi implementare lo snippet in cinque pagine diverse:

- [Home page](#home-page)
- [Lista prodotti](#lista-prodotti) 
- [Dettaglio prodotto](#dettaglio-prodotto)
- [Carrello](#carrello)
- [Pagina di conferma dell'ordine](#pagina-conferma)
- [Ricezione dei lead](#ricezione-dei-lead)

### Home page 
L'implementazione dello [snippet nella Home page](snippet_homepage.md) ci consente di monitorare i cosiddetti bouncer (ovvero gli utenti che  accedono alla Home page del sito e che poi lasciano il sito senza aver effettuato acquisti).

### Lista prodotti
Una pagina del catalogo che mostra un elenco di prodotti, ad esempio: una *pagina categoria* o una pagina *risultati della ricerca*, o una pagina *brand*. 
L'implementazione dello [snippet nella pagina lista articoli](snippet_pagina_ricerca.md) ci consente di monitorare l'interesse dell'utente verso un certo tipo di prodotto o categoria.

Molti utenti si limitano a navigare nelle pagine Categoria e Risultati della ricerca, senza fare clic per andare alle pagine Dettagli prodotto, e dunque l'implementazione in queste pagine di livello più elevato è la chiave per monitorare il comportamento di questi utenti.

### Dettaglio prodotto
La pagina Prodotto mostra i dettagli relativi a un prodotto specifico. L'installazione dello [snippet nelle pagine Prodotto](snippet_pagina_prodotto.md) è estremamente importante perché è proprio in quelle pagine che l'intento dell'utente si esprime in modo più compiuto. Vi sono molti utenti che accedono direttamente alle pagine Prodotto senza visitare prima le pagine Risultati della ricerca.

### Carrello
L'implementazione dello [snippet nella pagina Carrello](snippet_carrello.md), ci permette di monitorare quegli utenti che sono vicini alla conversione sul tuo sito ma che escono dal processo prima del pagamento finale.

### Pagina conferma
Quando un utente completa un acquisto sul tuo sito, essi vedranno una pagina di conferma delle vendite contenente un ID ordine e un riepilogo. 
Implementando lo [snippet nella pagina di conferma](snippet_pagina_conferma.md)  monitoreremo i prodotti che i tuoi clienti hanno acquistato.

Il monitoraggio di acquisti specifici ci permette di ottimizzare la distribuzione di offerte, in modo da non mostrare nuovamente al cliente prodotti che ha già acquistato od offerte a cui non è interessato.

### Ricezione dei lead
E' possibile ricevere automaticamente **in tempo reale** i dati dei lead generati per inserirli in flussi automatizzati, ad esempio **newsletter**, **email automation**, o altri sistemi di **remarketing**. Questo è anche indispensabile per effettuare la **deduplica** a monte e non pagare i contatti già posseduti.

Trovi tutti i dettagli nella sezione [webhook](webhook.html).

### Integrazioni opzionali o personalizzate
TODO

### Pagina generica
TODO

### Evento personalizzato di generazione Lead
TODO

### Invio manuale di una mail promozionale
TODO




