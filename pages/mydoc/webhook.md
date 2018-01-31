---
title: Webhook / lead tracking
sidebar: mydoc_sidebar
permalink: webhook.html
folder: mydoc
---

## Overview
**Transactionale** gestisce già la generazione dei lead per te, in modo assolutamente autonomo.

Ma sei hai altre potenzialità per poterli sfruttare, perché non approfittarne con i **webhook** di Transactionale?

Abbiamo creato questa feature per aiutarti ad **integrare nella tua piattaforma un’importazione automatica dei lead generati** e gestire autonomamente eventuali azioni di marketing in parallelo al nostro tracciamento.

Col webhook, **i lead ti vengono notificati direttamente e immediatamente** al momento della generazione (al click sull’offerta nel caso di opt-in implicito, dopo accettazione della privacy policy in caso di double opt-in).

Questo ti permetterà di usare i dati del lead per fini statistici, azioni di remarketing, o qualsiasi altro utilizzo tu possa ritenere utile.

Il webhook si sostituisce al tracciamento di Transactionale?
**No**. Transactionale continuerà comunque a tracciare i tuoi lead in modo autonomo sulla nostra piattaforma. Il webhook è solo una notifica parallela che consente di ampliare le possibilità della tua campagna a tuo piacimento.

## Come funziona
L’advertiser può configurare per il suo e-shop un URL (webhook URL) da chiamare con i dati del lead in modo da effettuare eventuali integrazioni nella loro piattaforma (ad es. inserimento in mailing list/newsletter, invio di conferma dell’offerta, altre offerte, ecc…)

Usando i webhook, è consigliabile disattivare nelle impostazioni della campagna l’invio della mail di conferma e dei reminder da parte di Transactionale, per non sovrapporre troppe comunicazioni.

## Implementazione tecnica
Verrà effettuata una chiamata POST con codifica ```application/x-www-form-urlencoded``` (quindi paragonabile alla submission di un comune form) contenente i seguenti parametri:

|Parametri| Descrizione|
|-------|------|
|ad_id|	l’id della campagna|
|email|	indirizzo email|
|first_name|	nome dell’utente|
|last_name|	cognome|
|gender|	sesso (“M” o “F”)|
|phone|	telefono|
|birth_year|	anno di nascita|
|coupon_code|	il codice coupon ricevuto dall’utente, facoltativo, utile in caso di campagne multi-coupon|
|zip_code|	cap dell’utente|

Ad esempio:
```
ad_id=72&email=test%40transactionale.com&coupon_code=TRCOUPON&first_name=Marianna&zip_code=12345
```

{% include callout.html content="<strong>Nota</strong>: dato che i lead provengono dalle aziende che, in Transactionale, svolgono il ruolo di publisher, quali dati sono effettivamente disponibili nella chiamata dipende da cosa il publisher riesce ad inviare. Riusciamo a garantire l’invio assolutamente certo di ad_id e email; riguardo i dati restanti, considerare sempre la possibilità che non siano sempre presenti." %}

## Gestione degli errori
Il contenuto della risposta non verrà considerato. I **codici di risposta >= 300** saranno considerati come errori, quindi il sistema potrebbe ritentare l’invio della richiesta.

## Deduplica
Il **codice di risposta 400** indica che l'indirizzo email è già esistente e quindi non vi sarà la generazione del lead.

