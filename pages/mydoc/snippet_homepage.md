---
title: Snippet nella home page
sidebar: mydoc_sidebar
permalink: snippet_homepage.html
folder: mydoc
---

## Panoramica
L'implementazione sulla Home page ci consente di monitorare i bouncer (ovvero gli utenti che  accedono alla Home page ma lasciano il sito senza effettuare acquisti). 

{% include_relative partials/loader_warning.md %}

```js
<script>
    // Track an event
    window._trx.push({
        event: 'viewHome'
    });
</script>
```