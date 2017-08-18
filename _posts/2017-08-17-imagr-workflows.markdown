---
layout: post
title:  "Included Workflows with imagr"
date:   2017-03-21 22:09:21 -0700
categories: macos imagr
---

Alternatively, how I took something off of the [imagr wiki](https://github.com/grahamgilbert/imagr/wiki) and turned it into a whole imaging operation.

In my current imagr setup, there are eight workflows, seven hidden, one visible. Of the hidden workflows, SCRIPTS-PKGS installs all the necessary first boot packages and scripts, so everything is automated, the other 6 are workflows to install specific versions of OS X, those being 10.9.5, 10.10.5, 10.11.6, 10.12.6, 10.13.x, and wishful thinking for 10.14.x.

Note that I have included sections in the config for 10.13 and 10.14, I am not running those in production. However, testing of 10.13 starts now, as the latest 10.13 beta (as of 08/17/17) has all the components necessary for imagr to operate.

The non-hidden workflow, named Workflow, runs a script to figure out which other workflows it should run. It figures this out via an API, utilized as a source of truth for the imaging workflow.

Below is an example:
{% gist ryanmoon/e5c96192aaadf832e59a6fed65807f4e %}

Note, that if you do run the `validateplist` tool from the imagr repo, it removes all comments from the document.

