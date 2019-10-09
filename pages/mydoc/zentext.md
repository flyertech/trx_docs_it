---
title:  "Migrazione API ZenText/Transactionale"
permalink: zentext_migration.html
sidebar: mydoc_sidebar
folder: mydoc
---

# Dismissione della piattaforma ZenText

## Introduzione

Da oggi, le funzionalità di ZenText sono state replicate all'interno della piattaforma Transactionale. La piattaforma ZenText verrà dismessa gradualmente.
La piattaforma Transactionale offre maggiore stabilità e scalabilità, oltre alla possibilità di accedere, se lo si desidera, alle funzionalità del network di cross-advertising per eCommerce.

Per i clienti che utilizzano ZenText per l'invio di SMS singoli tramite API, sarà sufficiente cambiare l'URL della chiamata.
Per tutti gli altri, sarà sufficiente ricaricare eventuali liste nella nuova piattaforma.

## Fasi della dismissione

### 14 ottobre 2019

Tutti gli account esistenti su ZenText vengono copiati su Transactionale mantenendo l'API KEY per l'eventuale utilizzo delle API.
E' necessario resettare la password, che non può essere trasferita.

Viene inviata una comunicazione via e-mail per comunicare ai clienti il passaggio.
In questa fase, non vengono trasferiti eventuali crediti residui. I clienti potranno farlo come descritto in seguito.

**IMPORTANTE** Solo l'account principale verrà trasferito. Transactionale non supporta ancora i multi-account.

## 18 novembre 2019

Verrà trasferito in automatico il credito residuo per tutti gli account che non hanno ancora provveduto.
Questo impedirà l'ulteriore invio di SMS tramite ZenText, producendo errori nelle eventuali chiamate all'API *send*.
La piattaforma resterà comunque a disposizione per consultazione.

## 16 dicembre

La piattaforma ZenText viene messa offline.

# Istruzioni operative

## Trasferimento del credito

All'accesso al nuovo account Transactionale, nella dashboard è presente il pulsante *Transfer credit*.
Il credito verrà trasferito in automatico e l'account ZenText di fatto reso di sola lettura.

**ATTENZIONE** Questa operazione non è reversibile.

## Migrazione API

L'API di invio di SMS singoli è retrocompatibile con la versione di ZenText.
Sarà quindi sufficiente cambiare il puntamento in questo modo:

```
# Indirizzo originale:
https://www.zentext.it/api/v1/send

# Nuovo indirizzo:
https://api.transactionale.com/platform/api/sms/send
```

La nuova API supporta anche funzionalità ulteriori. [Leggi la documentazione](send_sms.html).

# Domande frequenti

### Verranno trasferiti anche i prezzi applicati al mio account?

Sì, verranno trasferiti in automatico.

### Verranno trasferite le impostazioni dei webhook?

Sì, verranno trasferite. La nuova piattaforma ha anche nuove funzionalità riguardo ai webhook. [Leggi la documentazione](send_sms.html)

### Altre domande?

Scrivi a tech chiocciola transactionale.com (sostituisci chiocciola con @)