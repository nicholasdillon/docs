---
slug: secure-http-traffic-certbot
title: Secure HTTP Traffic with Certbot
description: "This quick answer shows how to use Certbot to secure your site's traffic via TLS."
authors: ["Edward Angert"]
contributors: ["Edward Angert"]
published: 2018-06-27
modified: 2020-12-02
keywords: ["let's encrypt", "certbot", "ssl", "tls", "https"]
tags: ["security", "web server"]
license: '[CC BY-ND 4.0](https://creativecommons.org/licenses/by-nd/4.0)'
aliases: ['/quick-answers/websites/secure-http-traffic-certbot/','/quick-answers/websites/certbot/secure-http-traffic-certbot/']
external_resources:
  - '[Certbot Official Documentation](https://certbot.eff.org/docs/)'
deprecated: true
deprecated_link: 'guides/enabling-https-using-certbot-with-nginx-on-ubuntu/'
---

## What is Certbot?

Certbot is a tool that automates the process of getting a signed certificate via [Let's Encrypt](https://letsencrypt.org/how-it-works/) to use with TLS.

For most operating system and web server configurations, Certbot creates signed certificates, manages the web server to accept secure connections, and can automatically renew certificates it has created. In most cases, Certbot can seamlessly enable HTTPS without causing server downtime.

## Before You Begin

Make sure you have registered a Fully Qualified Domain Name (FQDN) and set up [A and AAAA](/docs/guides/dns-overview/#a-and-aaaa) DNS records that point to your Linode's public [IPv4 and IPv6 addresses](/docs/products/compute/compute-instances/guides/manage-ip-addresses/). Consult our [DNS Records: An Introduction](/docs/guides/dns-overview/) and [DNS Manager](/docs/products/networking/dns-manager/) guides for help with setting up a domain.

{{< note >}}
If you're using Apache, change each instance of `nginx` to `apache` in the following sections.
{{< /note >}}

## Use Certbot on Debian

{{< content "certbot-shortguide-debian" >}}

## Use Certbot on Ubuntu

{{< content "certbot-shortguide-ubuntu" >}}

## Use Certbot on CentOS 7

{{< content "certbot-shortguide-centos" >}}

## Use Certbot to Renew All Certificates

You can renew all existing certificates that will expire in under 30 days with the following command:

    certbot renew
