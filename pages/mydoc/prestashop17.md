---
title:  "Come installare e configurare il plugin Prestashop >= 1.7"
permalink: prestashop17.html
sidebar: mydoc_sidebar
folder: mydoc
---


### Scarica l'ultima versione del plugin Prestashop
 Puoi scaricare l'ultima versione del plugin prestashop dalla sezione  **My Account -> Integration -> Select Prestashop >= 1.7**, clicca su **Download the plugin**

{% include image.html file="prestashop17/downloadplugin.png" url="images/prestashop17/downloadplugin.png" %}

### Installa il modulo

Nella sezione **Modules and Services** del tuo Prestashop installa il plugin appena scaricato. Al termine dell'installazione clicca su **Configure**

{% include image.html file="prestashop17/uploadplugin.png" url="images/prestashop17/uploadplugin.png" %}


### Dettaglio configurazione
Verrai reindirizzato alla pagina di configurazione del modulo
{% include image.html file="prestashop17/4.png" url="images/prestashop17/4.png" %}

Di seguito i dettagli dei campi visualizzati

*Auth Key*|utilizzata per identificare il tuo account. **Segui le istruzioni per copiarla qui**.
*Country*| le due lettere del codice ISO dove opera il tuo shop.
*Touchpoint Type*|come veicoli le offerte ai tuoi clienti. Può essere Mail, Web o Mail+Web.
*Web Touchpoint Id*|se utilizzi il touchpoint web, devi specificare un id, altrimenti prenderà un id di default.
*Web Touchpoint Text*|se utilizzi il touchpoint web, è possibile specificare il testo da visualizzare sopra le offerte.
*Automatically import leads*|abilita l'importazione automatica dei leads. Se abilitato, copia ed incolla l'URL visualizzato nel tuo account Transactionale su Account personale -> Integrazione -> URL webhook


{% include image.html file="prestashop17/5.png" url="images/prestashop17/5.png" %}

### Abilita/Disabilita Optin
E' necessario attivare l'opt-in dalla sezione di **Preferences -> Customers**.
{% include image.html file="prestashop17/optin.png" url="images/prestashop17/optin.png" %}

### Ultimi step

Copia la tua Auth Key dal tuo account Transactionale dalla sezione **My Account-> Integration** ed incollala nel campo Auth Key nella pagina di configurazione del modulo Prestashop

{% include image.html file="prestashop17/apikey.png" url="images/prestashop17/apikey.png" %}

Ricorda di Salvare le modifiche.

### Abilitare l'importazione automatica dei leads - Webhook

Per l'importazione automatica dei leads tramite webhook devi selezionare **YES** nel campo **Import leads automatically**

{% include image.html file="prestashop17/webhook.png" url="images/prestashop17/webhook.png" %}

Incolla il link che ti compare, nella sezione  **My Account-> Integration** del tuo account Transactionale nel campo **Webhook Url**

{% include image.html file="prestashop17/webhookurl.png" url="images/prestashop17/webhookurl.png" %}

Per verificarne il corretto funzionamento clicca su **Test**.