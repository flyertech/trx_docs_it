---
title:  "How to install and configure the Prestashop module"
permalink: prestashop16.html
sidebar: mydoc_sidebar
folder: mydoc
---


### Obtaining the latest Prestashop module

You can download the latest version from your dashboard by going to My Account -> Integration -> Select Prestashop and click on the Prestashop button.

### Installing the module

Go to the Modules page:

<div class='img-responsive'><img src="{{ site.url }}/assets/img/prestashop/modules_menu.png" /></div>

Click on the *Add new module* button:

<div class='img-responsive'><img src="{{ site.url }}/assets/img/prestashop/modules_buttons.png" /></div>

A form will appear where you can upload the module's zip file:

<div class='img-responsive'><img src="{{ site.url }}/assets/img/prestashop/module_upload.png" /></div>

After installing the module, you will need to enable it:

<div class='img-responsive'><img src="{{ site.url }}/assets/img/prestashop/module_installed.png" /></div>

Now click con the *Configuration* button to configure the module:

<div class='img-responsive'><img src="{{ site.url }}/assets/img/prestashop/module_configuration.png" /></div>

#### Settings details

*Auth Key*|this is used to identify your account. **Follow the instructions below to fill it**.
*Country code*|the two-letter ISO code for the country in which your shop operates. I.E. *IT*.
*Touchpoint Tyèe*|how to deliver offers to your customers. Make sure you configure your touchpoints in your Transactionale account
*Order confirmation touchpoint text*|if using the web touchpoint described above, you can specify the text to display above the offers.
*Automatically import leads*|Enable leads automatic import. When enabled, copy and paste the displayed URL into your Transactionale account at My Account -> Integration -> Webhook URL

### Last steps

Copy your Auth Key from your Transactionale account under My Account -> Integration:

<div class='img-responsive'><img src="{{ site.url }}/assets/img/integrate_api_key.png" /></div>

and paste it into the AUTH7 KEY field of the module configuration.

### Enabling automatic import of leads


