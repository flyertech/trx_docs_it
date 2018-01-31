L'integrazione consiste nell'inclusione di un tag Javascript che consente di acquisire le intenzioni dell'utente durante la navigazione del sito web.
Lo snippet è composto da due parti:

- Il [loader](snippet_loader.html), una libreria di Javascript che deve essere dichiarata in ogni pagina e si occupa della costruzione e dell'invocazione delle chiamate ai server Transactionale.

- Il tracker ci consente di acquisire gli eventi di navigazione dei visitatori del sito web (prodotti visti e acquistati), che quindi utilizziamo per determinare le raccomandazioni pertinenti e personalizzate.

Implementare il tracker è rapido, semplice ed invisibile per gli utenti. La qualità delle raccomandazioni dipende in modo diretto dalla qualità dell'implementazione del tracker, inclusi i tag installati in tutte le pagine, il trasferimento dei parametri corretti, etc.

Lo snippet:

- Non altera dal punto di vista visivo il sito ed è completamente invisibile per gli utenti.
- E' asincrono e non rallenta il caricamento delle pagine.
- Deve essere implementato nei punti corretti di ciascuna pagina del sito.