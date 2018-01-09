---
title: Snippet
sidebar: mydoc_sidebar
permalink: mydoc_snippet.html
folder: mydoc
---

## Panoramica
L'integrazione consiste nell'inclusione di un tag Javascript che consente di acquisire le intenzioni dell'utente durante la navigazione del sito web.
Lo snippet è composto da due parti:

- Il loader, una libreria di Javascript che deve essere dichiarata in ogni pagina e si occupa della costruzione e dell'invocazione delle chiamate ai server Transactionale.

- Il tracker ci consente di acquisire gli eventi di navigazione dei visitatori del sito web (prodotti visti e acquistati), che quindi utilizziamo per determinare le raccomandazioni pertinenti e personalizzate.

Implementare il tracker è rapido, semplice ed invisibile per gli utenti. La qualità delle raccomandazioni dipende in modo diretto dalla qualità dell'implementazione del tracker, inclusi i tag installati in tutte le pagine, il trasferimento dei parametri corretti, etc.

Lo snippet:

- Non altera dal punto di vista visivo il sito ed è completamente invisibile per gli utenti.
- E' asincrono e non rallenta il caricamento delle pagine.
- Deve essere implementato nei punti corretti di ciascuna pagina del sito.

## Dove dovresti implementare lo snippet
Devi implementare lo snippet in cinque pagine diverse:

- Home page
- Pagine di Ricerca/Elenco categorie
- Pagine relative ai prodotti
- Carrello
- Pagina di conferma dell'ordine

### Home page 
L'implementazione dello [snippet nella Home page](mydoc_snippet_homepage.md) ci consente di monitorare i cosiddetti bouncer (ovvero gli utenti che  accedono alla Home page del sito e che poi lasciano il sito senza aver effettuato acquisti). Valuteremo  automaticamente il valore di questi utenti e possiamo visualizzare banner con i prodotti più venduti.

### Pagina risultati di ricerca
Una pagina di presentazione della ricerca mostra più prodotti. Essa può essere una pagina categoria o una pagina risultati della ricerca. 
L'implementazione dello [snippet nella pagina risultati di ricerca](mydoc_snippet_pagina_ricerca.md) ci consente di monitorare l'interesse dell'utente verso un certo tipo di prodotto o categoria.

Molti utenti si limitano a navigare nelle pagine Categoria e Risultati della ricerca, senza fare clic per andare alle pagine Dettagli prodotto, e dunque l'implementazione in queste pagine di livello più elevato è la chiave per monitorare il comportamento di questi utenti.

### Pagina prodotto
La pagina Prodotto mostra i dettagli relativi a un prodotto specifico. L'installazione dello [snippet nelle pagine Prodotto](mydoc_snippet_pagina_prodotto.md) è estremamente importante perché è proprio in quelle pagine che l'intento dell'utente si esprime in modo più compiuto. Vi sono molti utenti che accedono direttamente alle pagine Prodotto senza visitare prima le pagine Risultati della ricerca.

### Carrello
L'implementazione dello [snippet nella pagina Carrello](mydoc_snippet_carrello.md), ci permette di monitorare quegli utenti che sono vicini alla conversione sul tuo sito ma che escono dal processo prima del pagamento finale.

### Pagina conferma
Quando un utente completa un acquisto sul tuo sito, essi vedranno una pagina di conferma delle vendite contenente un ID ordine e un riepilogo. 
Implementando lo [snippet nella pagina di conferma](mydoc_snippet_pagina_conferma.md)  monitoreremo i prodotti che i tuoi clienti hanno acquistato.

Il monitoraggio di acquisti specifici ci permette  di ottimizzare la visualizzazione del banner, in modo da non visualizzare al cliente nuovamente nei banner i prodotti che ha già acquistato.





