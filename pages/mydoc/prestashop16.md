---
title:  "Come installare e configurare il plugin Prestashop >= 1.6"
permalink: prestashop16.html
sidebar: mydoc_sidebar
folder: mydoc
---


### Scarica l'ultima versione del plugin Prestashop
Puoi scaricare l'ultima versione del plugin prestashop dalla sezione  **My Account -> Integration -> Select Prestashop <= 1.6**, clicca su **Download the plugin**

{% include image.html file="prestashop16/downloadplugin.png" url="images/prestashop16/downloadplugin.png" %}

### Installa il modulo

Nella sezione **Modules and Services** del tuo Prestashop clicca su **Add new module**, nel form che comparirà clicca su **Choose a file** seleziona il plugin scaricato e clicca su **Upload this module**.

{% include image.html file="prestashop16/1.png" url="images/prestashop16/1.png" %}

Comparirà la lista dei moduli, in particolare vedrai il modulo Transactionale appena scaricato. Dovrai cliccare su **Install**.

{% include image.html file="prestashop16/2.png" url="images/prestashop16/2.png" %}

Apparirà un popup, clicca su **Procedeed with installation**

{% include image.html file="prestashop16/3.png" url="images/prestashop16/3.png" %}

### Dettaglio configurazione
Verrai reindirizzato alla pagina di configurazione del modulo
{% include image.html file="prestashop16/4.png" url="images/prestashop16/4.png" %}

Di seguito i dettagli dei campi visualizzati

*Auth Key*|utilizzata per identificare il tuo account. **Segui le istruzioni per copiarla qui**.
*Country*|le due lettere del codice ISO dove opera il tuo shop.
*Touchpoint Type*|come veicoli le offerte ai tuoi clienti. Può essere Mail, Web o Mail+Web
*Web Touchpoint Id*|se utilizzi il touchpoint web, devi specificare un id, altrimenti prenderà un id di default.
*Web Touchpoint Text*|se utilizzi il touchpoint web, è possibile specificare il testo da visualizzare sopra le offerte.
*Import leads automatically*|abilita l'importazione automatica dei leads. Se abilitato, copia ed incolla l'URL visualizzato nel tuo account Transactionale su Account personale -> Integrazione -> URL webhook

{% include image.html file="prestashop16/5.png" url="images/prestashop16/5.png" %}

### Abilita/Disabilita Optin
E' necessario attivare l'opt-in dalla sezione **Preferences -> Customers**.
{% include image.html file="prestashop16/optin.png" url="images/prestashop16/optin.png" %}

### Ultimi step

Copia la tua Auth Key dal tuo account Transactionale dalla sezione **My Account-> Integration** ed incollala nel campo Auth Key nella pagina di configurazione del modulo Prestashop

{% include image.html file="prestashop16/apikey.png" url="images/prestashop16/apikey.png" %}

Ricorda di Salvare le modifiche.


### Abilitare l'importazione automatica dei leads - Webhook

Per l'importazione automatica dei leads tramite webhook devi selezionare **YES** nel campo **Import leads automatically**

{% include image.html file="prestashop16/webhook.png" url="images/prestashop16/webhook.png" %}

Incolla il link che ti compare, nella sezione  **My Account-> Integration** del tuo account Transactionale nel campo **Webhook Url**

{% include image.html file="prestashop16/webhookurl.png" url="images/prestashop16/webhookurl.png" %}

### Verifica integrazione e webhook

Puoi verificare il corretto funzionamento dell'integrazione tecnologica e del webhook url tramite queste semplici istruzioni:

{% include_relative partials/link_verify.md %}