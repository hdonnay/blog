---
layout: post
title: "Server Restructuring"
date: 2011-10-21 11:55
comments: false
categories: network
---
##kuro will be going down, and will come up a new man.
Mostly because I'm installing Debian on there to replace Arch. Arch, for
as much as I love it, lacks a few features I want, and its rolling cycle
isn't the best setup for a server OS.
<!--more-->

The big upgrade will be support for aufs, which means the stuff that's
spread across three drives will now appear to be one directory. Arch
requires a custom kernel for this, and its kernel is updated often
enough to make that a pain in the ass. Debian will also bring a larger
selection of (offical) packages. Users of hdonnay.net will notice a
small interruption in shell access, and a longer interruption in web
services, hopefully along the lines of an hour.

Shiro will be getting an upgrade as well, to a distro more suited to
it's use model. Currently, it's a custom install of Ubuntu that I fail
to update, because that breaks things. It will be switched over to
OpenELEC, which looks to be easier to administrate.

Also, repo.hdonnay.net has been set up as a CNAME to bitbucket.org, so
if you want to pretend that I'm providing you with git and mercurial
hosting, go ahead.
