---
title:  "Come installare e configurare il plugin Woocommerce"
permalink: woocommerce330.html
sidebar: mydoc_sidebar
folder: mydoc
---

### Scarica l'ultima versione del plugin Woocommerce
Puoi scaricare l'ultima versione del plugin Woocommerce dalla sezione **My Account -> Integration -> Select Woocommerce >= 3.3.0**, clicca su **Download the plugin**.

{% include image.html file="woocommerce/downloadplugin.png" url="/images/woocommerce/downloadplugin.png" %}

### Installa il modulo

Dalla sezione Plugin  del tuo WooCommerce clicca su **Carica plugin**.
{% include image.html file="woocommerce/1.png" url="/images/woocommerce/1.png" %}

Scegli file

{% include image.html file="woocommerce/2.png" url="/images/woocommerce/2.png" %}

ed infine installa ora

{% include image.html file="woocommerce/3.png" url="/images/woocommerce/3.png" %}

Verrai reindirizzato nella sezione Plugin e trovarei Trasactionale.

Se non hai specificato nessuna pagina di Termini e condizioni per il tuo Shop vedrai il link **Woocommerce Checkout Settings**

{% include image.html file="woocommerce/checkoutsettings.png" url="/images/woocommerce/checkoutsettings.png" %}

In questa pagina dovrai inserire la pagina in cui sono specificati **Termini e Condizioni** del tuo shop

{% include image.html file="woocommerce/termsandconditions.png" url="/images/woocommerce/termsandconditions.png" %}

Ricorda di salvare le modifiche.

Ritorna nella sezione  **Plugin**

clicca su **Settings** relativo al modulo Transactionale

{% include image.html file="woocommerce/5.png" url="/images/woocommerce/5.png" %}

### Dettaglio configurazione

Ti troverai nella pagina di configurazione del modulo

Di seguito i dettagli dei campi visualizzati

*Transactionale status*|seleziona Enabled per abilitare il plugin.
*Auth Key*|utilizzata per identificare il tuo account. **Segui le istruzioni per copiarla qui**.
*Country code*| le due lettere del codice ISO dove opera il tuo shop.
*Product Format*|indica il formato del prodotto che intendi inviare (Full o Id only).
*Touchpoint Type*|come veicoli le offerte ai tuoi clienti. Può essere Mail, Web o Mail+Web
*Web Touchpoint Id*|se utilizzi il touchpoint web, devi specificare un id, altrimenti prenderà un id di default.
*Web Touchpoint Text*|se utilizzi il touchpoint web, è possibile specificare il testo da visualizzare sopra le offerte.

{% include image.html file="woocommerce/6.png" url="/images/woocommerce/6.png" %}


### Ultimi step

Copia la tua Auth Key dal tuo account Transactionale dalla sezione **My Account-> Integration** ed incollala nel campo Auth Key nella pagina di configurazione del plugin WooCommerce.

{% include image.html file="woocommerce/apikey.png" url="/images/woocommerce/apikey.png" %}

Dopo aver compilato tutti i campi richiesti clicca su Save.

{% include image.html file="woocommerce/7.png" url="/images/woocommerce/7.png" %}