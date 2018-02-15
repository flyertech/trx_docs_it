---
title: Modalità di sviluppo
sidebar: mydoc_sidebar
permalink: debugging.html
folder: mydoc
---

## Modalità di sviluppo

Durante lo sviluppo, è possibile attivare un output di debug che mostrerà se e quali dati sono stati catturati dal Tag.
E' sufficiente inserire, prima del loader, lo snippet seguente:

```
window._trx_debug = true;
```

Questa modalità è testata su Google Chrome (o Chromium) e Mozilla Firefox.
Quando attiva, sarà possibile leggere in chiaro, nella console del browser, il contenuto del payload raccolto dal pixel.

Inoltre, dalla dashboard utente Transactionale, nella sezione *My account -> Integration* è possibile verificare l'effettiva ricezione dei diversi eventi.