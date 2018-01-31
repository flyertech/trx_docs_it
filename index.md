---
title: "Panoramica"
sidebar: mydoc_sidebar
permalink: index.html
folder: mydoc
summary: Dettagli integrazione v2

---

Questa è la **knowledge base tecnica di Transactionale**, dove potrai trovare tutti i dettagli e le spiegazioni tecniche per integrare il tuo e-Shop con Transactionale.

{% include callout.html content="Se il tuo shop è basato su **WooCommerce** o **PrestaShop** possiamo fornirti plug-in di integrazione già pronti, che potrai installare senza sforzo e che potranno essere completamente configurati dal tuo backend, senza praticamente nessun intervento tecnico." %}

# Funzionamento del network

## Advertiser {#advertiser}
Con **Transactionale** potrai coinvolgere nuovi clienti nel tuo e-Shop e tracciare le loro conversioni.

### Come coinvolgo nuovi clienti
Potrai in pochi passi creare una **campagna di advertising** e noi **la distribuiremo sul network**. I clienti di altri shop riceveranno le tue offerte, e le reclameranno sul tuo sito. Questo ti permetterà di acquisire **lead** qualificati di clienti reali che fanno acquisti online.

Se scegli anche di essere un [publisher](#publisher), puoi anche **monetizzare** e, se vuoi, reinvestire il guadagno in campagne di acquisizione, riducendone i costi.

### Gestione dei lead generati
Teniamo traccia di tutti i lead generati, permettendoti di monitorare sulla nostra piattaforma le prestazioni delle tue campagne.

Ma abbiamo anche la possibilità di **comunicare in tempo reale** al tuo sistema ogni **lead generato** per permetterti di raccogliere i dati dei lead anche direttamente sulla tua piattaforma. Questo consente l'integrazione con **newsletter**, sistemi di **email automation**, sistemi di **tracciamento**, **remarketing** o altro. Guarda la sezione sul [webhook](webhook.html) per i dettagli di implementazione. L'utilizzo del webhook è necessario per abilitare il sistema di **deduplica**.

## Publisher {#publisher}
Con **Transactionale** potrai monetizzare pubblicizzando offerte speciali per i tuoi clienti, facendoli felici e guadagnando.

### Come guadagno dal network
Quando Mario, uno dei tuoi clienti, **finalizza un ordine sul tuo e-shop**, Transactionale gli manderà delle offerte di altri shop del nostro network (complementari e non concorrenti). Ogni volta che un’offerta genera un lead (ovvero Mario clicca sull’offerta e atterra per la prima volta sul sito pubblicizzato), c’è un **guadagno** per te.

In aggiunta, se sei anche un [advertiser](#advertiser), potrai reinvestire i guadagni per la tua lead generation, riducendo i costi di acquisizione.

### Come funziona
1. Mario ordina sul tuo shop,
2. Ogni volta che **conclude un ordine** (cosa che in genere accade sulla **pagina di conferma dell’ordine**), il tuo shop **ci notifica** dell’avvenuto ordine tramite uno **snippet di tracciamento**,
3. Non appena riceviamo la chiamata, Transactionale manderà a Mario una **mail transazionale** con delle offerte,
4. Se Mario clicca su una delle offerte, verrà generato un **lead**.

# Cosa devi fare? Istruzioni tecniche

L'integrazione prevede due modalità:

  - [Integrazione completa](full_integration.html), **consigliata** per performance ottimali
  - [Integrazione semplificata](simplified_integration.html), performance *non ottimali*

