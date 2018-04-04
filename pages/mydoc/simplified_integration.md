---
title: Integrazione semplificata
sidebar: mydoc_sidebar
permalink: simplified_integration.html
folder: mydoc
---

## Panoramica
{% include_relative partials/integration_overview.md %}

{% include callout.html content="L'integrazione semplificata è sconsigliata per l'attività di publishing in quanto riduce quantità e qualità della profilazione automatica, e quindi riduce le performance di lead generation." %}

## Inserisci il tag in tutte le pagine
Il tag va inserito idealmente prima del tag di chiusura `</body>`.
Il tag include il loader, più l'evento `viewPage`:

{% include_relative snippets/loader_viewPage.md %}

## Inserisci il tag `trackTransaction` nella pagina di conferma ordine
Puoi inserire questo prima del tag di chiusura `</body>`, e in ogni caso dopo il loader, cioè lo snippet che va inserito in ogni pagina mostrato nel paragrafo precedente.
Dovrai riempire tutti i campi disponibili con i valori effettivi relativi all'ordine appena concluso.

{% include_relative snippets/tracktransaction.md %}

## Selezione automatica touchpoint
Inserendo in touchpointType auto, in base ai campi compilati verrà attivato automaticamente il touchpoint di tipo mail o web. Nel caso in cui venga attivato il touchpoint di tipo web e non è stato inserito il touchpointId, quest'ultimo sarà assegnato con un valore di default.

## Touchpoint web
Se utilizzi il touchpoint web dovrai specificare dove vuoi che vengano mostrate le offerte nella tua pagina perciò dovrai inserire un `<div id="tr_touchpoint_container"></div>` nel punto in cui desideri. Verrà visualizzato il seguente banner con layout orizzontale.

![image-title-here](images/banner_horizontal.png){:class="img-responsive"}

Aggiungendo la classe `tr-touchpoint-layout-vertical` nel `<div>` in questo modo:<br>
 `<div id="tr_touchpoint_container" class="tr-touchpoint-layout-vertical"></div>` <br>
 il banner avrà layout verticale:

![image-title-here](images/banner_vertical.png){:class="img-responsive"}
