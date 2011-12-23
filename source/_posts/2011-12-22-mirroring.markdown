---
layout: post
title: "Mirroring"
date: 2011-12-22 23:22
comments: false
categories: server
---
I set up gitolite on the home server, which is pretty slick. The only
thing it doesn't do automagically is mirroring to other repositories.

It has a mechanism to mirror to other gitolite installations, but
things like github don't work. I needed to write custom post-receive
hooks like so:

    #!/bin/sh
    git push --mirror git@github.com:hdonnay/project.git

Really damn easy, but not automated, which is lame.
