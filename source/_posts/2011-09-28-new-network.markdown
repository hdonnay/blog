---
layout: post
title: "New Network"
date: 2011-09-28 11:43
comments: false
categories: networking
---
This has been negelected for a while, but that's okay, because no one
reads it.

My network topology has undergone some change, and this is my attempt
at documenting it.
<!--more-->

First off, this site has been pulled off my home server and thrown up on
a free(!) [Amazon EC2][ec2] micro-instance. Granted, it's only free for a year,
and then only free for new [Amazon Web Services][aws] customers, but that means
I have an actual remote server that I can't walk over and turn off!
Exciting!

I've also moved into a new place, and I'm using a new router. This
router is native IPv6 capable and can also use a tunnel. That means I
don't have to have a tunnel on my server anymore, I can offload it to
the router. The new router has a whole bunch of cool functions that I
haven't played with yet, because I don't want to bring down the network
for everyone.

I also have a new Windows PC, which meant I had to switch my server off
of NFS and onto Samba. This was kicking my ass until I realized I had
the wrong subnet specified in my config. \-\_\- oops. That being said,
Windows plays surprisingly nice with my setup, and it's nice to be able
to run a local GUI for my [Deluge][deluge] daemon.

My mailserver was switched from [Postfix][postfix] to [Exim][exim], and
works now. I was put off of using Exim after hearing that its config was
dense and confusing, and this is somewhat true -- although less than I'd
thought, it comes with a working config by default. That seems
blindingly obvious, but it's the only mailserver that does that.
Granted, [Comcast][comcast] doesn't allow traffic over port 25, so I
can't use it. I pointed my MX records at [Google Apps][apps] and that's
taken care of all the mail (read: none) that I get.

I recently updated [nzbd][sabnzbd], [SickBeard][sickbeard],
[CouchPotato][couchpotato], and [Headphones][headphones] to their git
versions. By virtue of them being written in Python, this means I can just
do a `git pull` in the proper directory to update them. I also hacked
this blog (powered by [Octopress][octopress]) to be completely modular,
can able to be updated from anywhere that I can pull from my git repo.

I can't think of anything else I've hacked up. I wanted to set up YAWS,
but Apache works just fine, and comes packaged on this EC2 instance.

[ec2]: https://aws.amazon.com/ec2/
[aws]: https://aws.amazon.com/
[deluge]: http://deluge-torrent.org/
[postfix]: http://www.postfix.org/
[exim]: http://www.exim.org
[comcast]: http://comcastsucks.org/
[apps]: http://www.google.com/apps/intl/en/group/index.html
[sabnzbd]: http://www.sabnzbd.org/
[sickbeard]: http://sickbeard.com/
[couchpotato]: http://www.couchpotatoapp.com/
[headphones]: https://github.com/rembo10/headphones
[octopress]: http://www.octopress.org/
