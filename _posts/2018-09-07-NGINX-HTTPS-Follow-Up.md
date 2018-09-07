---
layout: post
title: NGINX+HTTPS Follow Up
tags:
  - security
  - tutorial
  - web
---

Many moons ago I wrote a tutorial about how to imbue your NGINX server with SLL
using the EFF's [`certbot`<i class="fa
fa-external-link"></i>][certbot]{:target="_blank"} (which you can read
[here][nginx post]).

Well, by my estimation (from looking at `certbot`'s [release schedule<i class="fa
fa-external-link"></i>][certbot github]{:target="_blank"} on GitHub) I was
using v0.22.2, which is 5 minor releases behind the current 0.27.1 version.
And, in my usage of the tool, I've found that NGINX mode has come a long way.

<!-- MORE -->

Now, all you need to do is have a bare-bones configuration in `sites-enabled`
for `certbot` to detect, e.g.:

    # /etc/nginx/sites-enabled/foo.conf
    server {
        listen 80;
        server_name foo.com;
    }

Then simply run:

    $ sudo certbot --nginx

and follow the prompts.

`certbot` will make the necessary changes to the configuration files and
install your new certificates in the appropriate locations.

When you need to renew your certificates, simply rerun the command above.



[certbot]:        https://certbot.eff.org
[nginx post]:     {% post_url 2017-03-31-NGINX-+-HTTPS %}
[certbot github]: https://github.com/certbot/certbot/releases
