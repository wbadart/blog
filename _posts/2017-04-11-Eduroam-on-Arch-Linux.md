---
title: Eduroam on Arch Linux
tags:
  - arch linux
  - tutorial
date: 2017-04-11 21:02:59
categories:
  - ethics
layout: post
---


Before we begin, I just want to mention that I have posts about **AI and automation** in the works, so get hyped for those. Before I publish those, however, I wanted to put out this tutorial on connecting to Notre Dame's Eduroam network on Arch Linux because I struggled with it for several days and just found a solution.

1. Get your hands on `wpa_supplicant` and `connman`. `connman` comes from the AUR, so you'll need to use `pacaur`, `yaourt`, or some other AUR enabled `pacman` wrapper (unless you've already configured `pacman` to be AUR enabled, in which case, you're good to go!). [Here's](https://wiki.archlinux.org/index.php/AUR_helpers) the list of so-called "AUR helpers" from the Arch wiki.

    ```
    $ yaourt -S connman wpa_supplicant
    ```

2. Add a `connman` configuration for Eduroam. Save the following to `/var/lib/connman/eduroam.config`, replacing *mynetid* and *mypassword* with your Notre Dame netid and password respectively (see [the wiki](https://wiki.archlinux.org/index.php/Connman#Connecting_to_eduroam) page on `connman` for reference).

    ```
    [service_eduroam]
    type=wifi
    Name=eduroam
    EAP=peap
    CACertPath=/etc/ssl/certs
    Phase2=MSCHAPV2
    Identity=mynetid@nd.edu
    AnonymousIdentity=anonymous@nd.edu
    Passphrase=mypassword
    ```

3. Enable the services so they start at boot.

    ```
    $ systemctl enable wpa_supplicant connman
    ```

4. Restart both of those services to connect (`systemctl restart wpa_supplicant connman`). Alternatively, reboot your computer to make sure the whole auto-startup business works. This is the profit step; you should be connected once it's done.

An interesting thing that I'll note before leaving you is that when I'm connected to Eduroam, I've found that I can access the internet just fine (browse the web, curl around, ssh into the blog server, etc.) but I don't get replies from `ping`s. Not sure what the deal is here, but just thought I'd mention it FYSA.

