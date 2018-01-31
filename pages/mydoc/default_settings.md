---
title: Overriding default settings
sidebar: mydoc_sidebar
permalink: mydoc_default_settings.html
folder: mydoc
---

## Overview
??

## Snippet esempio

Codice di esempio

```js
<script src="/integration/v2/main.js" async="true"></script>
<script>
    // Enable debug mode: it will a expose the internal attributes on _trx._debug
    window._trx_debug = true;
    window._trx = window._trx || [];
    window._trx.push(
    // Configuring the tracker
    {
      event: "setConfig", 
      config: {
        // Point to your local env during development
        baseUrl: 'http://local.transactionale.com',
        // Server-side tracker endpoint
        endpoint: 'http://local_trx.transactionale.com',
        // Manually issue a flush event to send data to the server
        autoSend: false
      }
    },
    {
        event: 'setAccount', account: 'API-KEY', country: 'IT'
    });
</script>
```



