---
title:  "Come installare e configurare il plugin Magento"
permalink: magento.html
sidebar: mydoc_sidebar
folder: mydoc
---

### Scarica l'ultima versione del plugin Magento
 Puoi scaricare l'ultima versione del plugin Magento dalla sezione **My Account -> Integration -> Select Magento 1.x**, clicca su **Download the plugin**.

{% include image.html file="magento/downloadplugin.png" url="images/magento/downloadplugin.png" %}

### Disinstalla la vecchia versione del modulo
Se avevi già installato il plugin di Magento procedi prima con la disistallazione dello stesso.

{% include image.html file="magento/unistall.png" url="images/magento/unistall.png" %}

### Installa il modulo

Da **Magento Connect Manager** clicca su **Scegli File** poi **Upload**.

{% include image.html file="magento/connectmanager.png" url="images/magento/connectmanager.png" %}

Clicca sul **Settings** di Transactionale.

{% include image.html file="magento/settings.png" url="images/magento/settings.png" %}

### Dettaglio configurazione

Ti troverai alla pagina generica di configurazione del modulo.

Di seguito i dettagli dei campi visualizzati:

*Sending mode*| Client side (Javascript) di default. Se hai un checkout customizzato seleziona l'altra opzione.
*Mode*| Ruolo in Transactionale (Publisher and Advertiser, solo Publisher, solo Advertiser, Disabilitato).
*Debug*| seleziona No.
*Auth Key*|utilizzata per identicare il tuo account. **Segui le istruzioni per copiarla qui**.
*Import leads automatically*|abilita l'importazione automatica dei leads. Se abilitato, copia ed incolla l'URL visualizzato nel tuo account Transactionale su Account personale -> Integrazione -> URL webhook

{% include image.html file="magento/configuration.png" url="images/magento/configuration.png" %}

Dovrai anche completare la configurazione per il singolo store.

Di seguito i dettagli dei campi visualizzati:

*Country Code*| le due lettere del codice ISO dove opera il tuo shop.
*Touchpoint Type*| seleziona Auto
*Web Touchpoint Id*| se utilizzi il touchpoint web, devi specificare un id, altrimenti prenderà un id di default.
*Web Touchpoint Text*| se utilizzi il touchpoint web, è possibile specificare il testo da visualizzare sopra le offerte.
*Opt-in Privacy Link* | link della tua privacy policy.

{% include image.html file="magento/configuration_store.png" url="images/magento/configuration_store.png" %}

### Ultimi step

Copia la tua Auth Key dal tuo account Transactionale dalla sezione **My Account-> Integration** ed incollala nel campo Auth Key nella pagina di Settings.

{% include image.html file="magento/apikey.png" url="images/magento/apikey.png" %}

Dopo aver compilato tutti i campi richiesti salva le modifiche.


### Abilitare l'importazione automatica dei leads - Webhook

Per l'importazione automatica dei leads tramite webhook devi selezionare **YES** nel campo **Import leads automatically**.

{% include image.html file="magento/webhook.png" url="images/magento/webhook.png" %}

Incolla il link che ti compare, nella sezione  **My Account-> Integration** del tuo account Transactionale nel campo **Webhook Url**

### Verifica integrazione e webhook

Puoi verificare il corretto funzionamento dell'integrazione tecnologica e del webhook url tramite queste semplici istruzioni:

{% include_relative partials/link_verify.md %}