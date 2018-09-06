---
title: Cloud Adventure pt. 2
tags:
  - cloud
  - tutorial
date: 2017-04-02 20:44:52
categories:
  - ethics
layout: post
---


This is a casual sequel to [last week's tutorial](https://blog.wbadart.info/2017/03/31/NGINX-HTTPS) on getting nginx set up with HTTPS. Towards the end of that post, I dropped a reference to a new subdomain on `wbadart.info`, `cloud.wbadart.info`. This new record points to my installation of [Nextcloud](https://nextcloud.com), an open source, self-hosted alternative to such cloud-storage services as Google Drive and Box.

<!-- MORE -->

Here's a quick tutorial on getting Nextcloud set up behind your PHP-enabled web server.

## Nextcloud tutorial

1. Go through the [list of prerequisites](https://docs.nextcloud.com/server/11/admin_manual/installation/source_installation.html#prerequisites) and install them on your system. (PHP modules are typically available through your package manager though the package `php-modulename` or `php7.0-modulename`.)

2. I used the web installer since that seemed the easiest. [Here](https://download.nextcloud.com/server/installer/setup-nextcloud.php)'s the download link. Download this to `/var/www/html` or wherever your web root is.

3. Visit your site at `setup-nextcloud.php`, i.e. `mydomain.com/setup-nextcloud.php` and follow the prompt.

And that's about all she wrote. Most of the snags I ran into were solved either by doing `chown -R www-data:www-data /var/www/html`, `chmod -R 755 /var/www/html` and starting over from scratch.

{% include youtube.html v="NeSuNi6YARU" %}

## Reflection

I think the saying "If you're not paying for the product, your are the product" is certainly true with respect to cloud services. Now, having seen how easy it is to set up your own cloud service with something like Nextcloud, that trade-off of privacy for convenience is absolutely not worth it. I think for a more complicated service like email, it'll still be worth it (though I'm sure I'll keep poking at iRedMail when I have the time).

I can't say I have a moral objection to the privacy encroachments by cloud services. It would be one thing to harvest our data in secret, but it's pretty much all laid out in the various EULAs and Privacy Policies. Now, just because I have no moral objections to these collections doesn't mean I want them done on my data. I think I'll continue to try my hand in private cloud services. Stay tuned for future posts and tutorials!

