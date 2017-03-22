---
layout: post
title:  "Serving Up Munki With Nginx on MacOS"
date:   2017-03-21 22:09:21 -0700
categories: macos munki nginx
---

The place where I work has a lot of Mac Minis, and while you can install a Linux OS on a Mac Mini, you have to do it by hand, not via a PXE boot or something similar[1]. So I went about building some Munki servers on MacOS using chef, and nginx.

This setup assumes the following:
- 1) The content for the Munki server is version controlled, my example will use GitHub and git.
- 2) The large items, the pkgs/disk images are stored in a separate service, my example will use s3.
- 3) Chef is used for configuration management


[1] Or at least that's what my Google searches return.
