---
title: Snippet loader
sidebar: mydoc_sidebar
permalink: snippet_loader.html
folder: mydoc
---

## Descrizione
Il loader è la parte comune del tag di integrazione, che va inserita nel tag `<head>` del sito, e prima degli altri snippet:

{% include_relative snippets/loader.md %}

## Configurazione

1. Preleva l'api key dalla sezione My Account -> Integration del tuo profilo Transactionale ed sostituiscila ad `**API-KEY**`.
2. Inserisci il codice ISO a 2 lettere della nazione del sito come valore della chiave `country`.