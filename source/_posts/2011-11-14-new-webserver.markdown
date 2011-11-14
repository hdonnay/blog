---
layout: post
title: "New webserver"
date: 2011-11-14 11:22
comments: false
categories: website
---
The site is different, again.
===
You hopefully haven't noticed, but I changed the http server that
hdonnay.com runs on.

<!--more-->
It used to be Apache, the "default" webserver, but I've changed it to
nginx. Why? Two reasons:
    * The site is almost completely static files, which nginx does
      better than Apache.
    * I hadn't changed anything on the server for almost two weeks.

The home server still runs Apache, but the traffic is so low there and
it's mostly used for proxying to other apps, so I don't think that it
justifies all the reconfiguring that it would entail.
