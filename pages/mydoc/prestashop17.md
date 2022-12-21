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

Per installare Transactionale sul vostro sito Prestashop, sarà necessario loggare nel backend ed accedere alla sezione “**Moduli → Gestisci moduli**”, presente sulla sidebar destra.

{% include image.html file="prestashop17/01.png" url="images/prestashop17/01.png" %}

Dopo essere entrati nella sezione, in alto a destra ci sarà un pulsante su cui cliccare, ossia “**Carica un modulo**” 

{% include image.html file="prestashop17/02.png" url="images/prestashop17/02.png" %}

Comparirà questa schermata: 

{% include image.html file="prestashop17/03.png" url="images/prestashop17/03.png" %}

A questo punto carichiamo il file zip del nostro modulo:

{% include image.html file="prestashop17/04.png" url="images/prestashop17/04.png" %}

Cliccare su “**Configura**” per passare alla configurazione.

### Dettaglio configurazione
Di seguito, la schermata che si presenterà nel processo di configurazione di Transactionale:

{% include image.html file="prestashop17/05.png" url="images/prestashop17/05.png" %}

Analizziamo le singole voci per scegliere la configurazione desiderata:

---

**Attivazione/Disattivazione Transactionale**
Per attivare o disattivare Transactionale, si può disattivare/attivare direttamente il modulo da
Prestashop.

---

**Auth Key**
Codice identificativo fornito da Transactionale (Segui le istruzioni per copiarlo qui)

---

**Country Code**
Il codice ISO di due lettere per il paese in cui opera il tuo negozio (esempio: it. en, etc…)

---

**Touchpoint Type**
Dalla tendina si potrà scegliere uno dei seguenti touchpoint, ossia il campo su cui si vuole
agire:
- **Email** → Verrà inviata solo la mail relativa alle offerte riservate;

- **Web** → Verrà mostrato solo il banner relativo alle offerte riservate;

- **Auto (Web + Mail)** → Campo dipendente dalla scelta dell’utente in merito alla dicitura “Ricevi offerte dai nostri partner” presente di default su Prestashop.

{% include image.html file="prestashop17/06.png" url="images/prestashop17/06.png" %}

Solo selezionando **Web e Mail + Web**, compaiono due voci extra, strettamente legate al banner, ossia: 
- **Web Touchpoint Id** → Va inserito l’ID del div che è stato impostato nel template per essere popolato con le informazioni del banner (se utilizzi il touchpoint web, devi specificare un id, altrimenti prenderà un id di default);

- **Web Touchpoint Text** → Titolo banner visualizzato, in questo caso “Ci sono delle offerte per te” .

{% include image.html file="prestashop17/07.png" url="images/prestashop17/07.png" %}

### Schema riepilogativo
{% include image.html file="prestashop17/08.png" url="images/prestashop17/08.png" %}

### Ultimi step

Copia la tua Auth Key dal tuo account Transactionale dalla sezione **My Account-> Integration** ed incollala nel campo Auth Key nella pagina di configurazione del modulo Prestashop

{% include image.html file="prestashop17/apikey.png" url="images/prestashop17/apikey.png" %}


### Verifica integrazione

Puoi verificare il corretto funzionamento dell'integrazione tecnologica e del webhook url tramite queste semplici istruzioni:

{% include_relative partials/link_verify_integration.md %}