---
title:  "Come installare e configurare il plugin Woocommerce"
permalink: woocommerce330.html
sidebar: mydoc_sidebar
folder: mydoc
---

### Scarica l'ultima versione del plugin Woocommerce
Puoi scaricare l’ultima versione del plugin Woocommerce dalla sezione **My Account -> Integration -> Select Woocommerce ->** clicca su **Download the plugin**.

{% include image.html file="woocommerce/downloadplugin.png" url="images/woocommerce/downloadplugin.png" %}

### Installa il modulo

Per poter installare il plugin di Transactionale, sarà necessario accedere al backend del proprio sito e navigare nella sezione **Plugin**:
{% include image.html file="woocommerce/1.png" url="images/woocommerce/1.png" %}

Clicca su **“Aggiungi nuovo”** 

{% include image.html file="woocommerce/02.png" url="images/woocommerce/02.png" %}

Cliccare su **“Carica Plugin”**

{% include image.html file="woocommerce/03.png" url="images/woocommerce/03.png" %}

Caricare il file zip del plugin, cliccando sul tasto **“Scegli file”**

{% include image.html file="woocommerce/04.png" url="images/woocommerce/04.png" %}

Successivamente, cliccare su **“Installa adesso”**

{% include image.html file="woocommerce/05.png" url="images/woocommerce/05.png" %}

Dopo l’installazione del plugin, verrà aggiunta una voce alla sidebar, ossia “Transactionale”

{% include image.html file="woocommerce/06.png" url="images/woocommerce/06.png" %}

Dopo l’installazione, si passa alla configurazione del plugin.

### Configurazione plugin Wordpress

Di seguito la schermata che si presenterà nel processo di configurazione di Transactionale:

{% include image.html file="woocommerce/07.png" url="images/woocommerce/07.png" %}

Analizziamo le singole voci per scegliere la configurazione desiderata: 

---

**Transactionale Status**

- **Enable** → Transactionale sarà attivo ed utilizzabile; 
- **Disabled** → Transactionale verrà disattivato.

---

**Auth Key**
Codice identificativo fornito da Transactionale

---

**Country Code**
Il codice ISO di due lettere per il paese in cui opera il tuo negozio (esempio: it. en, etc…)

---

**Show 3rd Party Opt-In checkbox***
- **Enable** → Abilitando questa funzionalità, viene mostrata la seguente dicitura, in fase di checkout: 
{% include image.html file="woocommerce/08.png" url="images/woocommerce/08.png" %}
- <ins>Cosa succede se si spunta la casella per accettazione</ins>: Viene inviata una mail ma non compare il banner;
- <ins>Cosa succede se non si spunta la casella per accettazione</ins>: Non viene inviata mail ma viene mostrato solo il banner 
- **Disabled** → Non viene mostrata la dicitura indicata in fase di checkout ed automaticamente non viene inviata mail ma mostrato solo il banner.

*Questa funzionalità è strettamente legata a Wordpress.

---

**Touchpoint Type**
Dalla tendina si potrà scegliere uno dei seguenti touchpoint, ossia il campo su cui si vuole agire:
- **Email** → Verrà inviata solo la mail relativa alle offerte riservate; 
- **Web** → Verrà mostrato solo il banner relativo alle offerte riservate;
- **Auto (Web + Mail)** → Campo dipendente dalla scelta dell’utente in merito alla 3rd party opt-in checkbox.

Solo selezionando Web e Auto, compaiono due voci extra, strettamente legate al banner, ossia: 
- **Web Touchpoint Id** → Va inserito l’ID del div che è stato impostato nel template per essere popolato con le informazioni del banner; 
- **Web Touchpoint Text** → Titolo banner visualizzato, in questo caso “Le offerte a te riservate”.
{% include image.html file="woocommerce/09.png" url="images/woocommerce/09.png" %}

### Schema riepilogativo
{% include image.html file="woocommerce/10.png" url="images/woocommerce/10.png" %}

*Solo per Wordpress 


### Ultimi step

Copia la tua Auth Key dal tuo account Transactionale dalla sezione **My Account-> Integration** ed incollala nel campo Auth Key nella pagina di configurazione del plugin WooCommerce.

{% include image.html file="woocommerce/apikey.png" url="images/woocommerce/apikey.png" %}

### Verifica integrazione

Puoi verificare il corretto funzionamento dell'integrazione tecnologica e del webhook url tramite queste semplici istruzioni:

{% include_relative partials/link_verify_integration.md %}