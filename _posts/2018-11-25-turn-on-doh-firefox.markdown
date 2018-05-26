---
layout: post
title:  "Turn on DOH in Firefox!"
date:   2017-05-25 12:01:33 
categories: firefox dns
---

# DOH DNS over HTTPS in Firefox

[from]: https://www.comss.ru/page.php?id=4950 

**about:support**

Check version

**about:config**

*network.trr.mode* 2 or 3

*network.trr.uri*

  https://mozilla.cloudflare-dns.com/dns-query

  https://dns.google.com/experimental

*network.trr.bootstrapAddress*

  1.1.1.1

  8.8.8.8

**about:networking**

  dns


