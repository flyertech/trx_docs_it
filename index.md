---
title: "Panoramica"
sidebar: mydoc_sidebar
permalink: index.html
folder: mydoc
summary: Dettagli integrazione v2

---

Questa è la **knowledge base tecnica di Transactionale**, dove potrai trovare tutti i dettagli e le spiegazioni tecniche per integrare il tuo e-Shop con Transactionale.

## Advertiser {#advertiser}
Con **Transactionale** potrai coinvolgere nuovi clienti nel tuo e-Shop e tracciare le loro conversioni.

### Come coinvolgo nuovi clienti
Potrai in pochi passi creare una **campagna di advertising** e noi **la distribuiremo sul network**. I clienti di altri shop riceveranno le tue offerte, e le reclameranno sul tuo sito. Questo ti permetterà di acquisire **lead** qualificati che hanno un tasso di conversione più alto rispetto ad altri metodi di acquisizione clienti.

Se scegli anche di essere un [publisher](#publisher), puoi anche **guadagnare** e, se vuoi, reinvestire il guadagno nella tua campagna riducendo ulteriormente i costi di acquisizione.

### Come funziona
{% include callout.html content="Se il tuo shop è basato su **WooCommerce** o **PrestaShop** possiamo fornirti plug-in di integrazione già pronti, che potrai installare senza sforzo e che potranno essere completamente configurati dal tuo backend, senza praticamente nessun intervento tecnico." %}

In tutti gli altri casi, basta semplicemente includere uno **snippet di codice JavaScript (lato client)** su **tutte le pagine** del tuo sito web, come spiegato più avanti.

Questo codice traccerà gli utenti che arrivano sul tuo sito e mostrerà loro il popup tramite il quale si può reclamare la loro offerta.

### Webhook e tracciamento lead
Noi teniamo traccia di tutti i lead generati (insieme a tanti altri dati), permettendoti di monitorare sulla nostra piattaforma le prestazioni delle tue campagne.

Ma abbiamo anche la possibilità di **comunicare in tempo reale** al tuo sistema ogni **lead generato** per permetterti di raccogliere i dati del lead anche direttamente sulla tua piattaforma. Questo apre a molte possibilità, come sfruttare i nostri dati per meccanismi di tracciamento/statistica, remarketing o altro: guarda la sezione sui [webhook](mydoc_webhook.html) per i dettagli di implementazione.

### [Cosa devo fare - Dettagli tecnici](mydoc_snippet.html)


## Publisher {#publisher}
Con **Transactionale** potrai monetizzare pubblicizzando offerte speciali per i tuoi clienti, facendoli felici e guadagnando.

### Come guadagno dal network
Quando Mario, uno dei tuoi clienti, **finalizza un ordine sul tuo e-shop**, Transactionale gli manderà delle offerte di altri shop del nostro network (complementari e non concorrenti), con due benefici:

1. aumenti **il gradimento dell’esperienza di acquisto** di Mario perché gli presenti offerte interessanti,
2. ogni volta che un’offerta genera un lead (ovvero Mario clicca sull’offerta e atterra per la prima volta sul sito pubblicizzato), c’è un **guadagno** per te.

In aggiunta, se sei anche un [advertiser](#advertiser), potrai reinvestire i guadagni per la tua lead generation, riducendo i costi di acquisizione.

### Come funziona
1. Mario ordina sul tuo shop,
2. Ogni volta che egli **finalizza un ordine** (cosa che in genere accade sulla **pagina di conferma dell’ordine**), il tuo shop **ci notifica** dell’avvenuto ordine tramite una **chiamata al nostro server**,
3. Non appena riceviamo la chiamata, Transactionale manderà a Mario una **mail transazionale** con le offerte,
4. Se Mario clicca su una delle offerte, verrà generata un **lead**.

Se il tuo shop è basato su **WooCommerce** o **PrestaShop** possiamo fornirti plug-in di integrazione già pronti, che potrai installare senza sforzo e che potranno essere completamente configurati dal tuo backend, senza praticamente nessun intervento tecnico.

Per tutti gli altri scenari, puoi rendere possibile l’invio dell’email transazionale col nostro semplice **snippet di integrazione manuale**, come spiegato dopo.

### [Cosa devo fare - Dettagli tecnici](mydoc_snippet.html)
