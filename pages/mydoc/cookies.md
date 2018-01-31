---
title: Cookies
sidebar: mydoc_sidebar
permalink: mydoc_cookies.html
folder: mydoc
---

##Overview


### Host cookies


- __trx: A simple flag that shows that the TRX pixel ran at least once
- __trx_cht: Check-in time - It stores when the users has last landed on the website after clicking on a Transactionale Ad
- __trx_tid: TouchPoint ID - Identifies the touchpoint that delivered the offer to the user
- __trx_bid: Booking id - Identifies the combination of Ad/Channel the user clicked on
- __trx_bhs: Booking Hash - A checksum that allows checking the integrity of the tracking data
- __trx_uhs: User Hash - A checksum that identifies the user who received the offer anonymously
- __trx_ths: Transaction Hash - A checksum that identifies the mail that originated the visit
- __trx_uid: User ID - Local to the website executing the JS integration
- __trx_ext: Boolean - True if the has user already been shown the exit overlay

### Tracking server cookies


- __trx_uid: User ID - Common across all the websites in the network, unless the __trx_optout cookie is set.
- __trx_optout: Stores the opt-out preference of a user

### Cookie law compliance
It is up to the user to correctly implement this integration in compliance with the EU privacy law. However, we provide a simple opt-out page for end users.

This will not disable the system. It will simply inhibit tracking, and thus the quality of the recommendations delivered to the user.

Users’ IP addresses are anonimzed before storage. All behavioural information is stored in anonimized form. All personal information is stored on a separate database. These two features are designed to make us unable to match the information across the two databases.

See: http://www.criteo.com/privacy/

To manage your privacy settings: https://www.transactionale.com/privacy-settings
