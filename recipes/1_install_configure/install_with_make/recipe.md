<!--
name: install-with-make
freshnessDate: 2013-01-12
version : "0.9"
title : "Install Redis With Make"
description: "Part of the Redis Cookbook, http://www.rediscookbook.org"
homepage : "http://www.rediscookbook.org"
author : "Ted Nyman"
license : "CC Attribution Share Alike 3.0"
-->

<!-- @section -->

### Problem

You want to install Redis on Linux, OS X, or a similar Posix operating system.

### Solution

Redis is literally 'zero-configuration.' Download the most recent Redis [stable release](http://code.google.com/p/redis/).
Untar the file into a new directory and `cd` into that directory. Now, run `make`. Redis
is now installed and configured using the default configuration. Run `./redis-server`
to start the server and you're done.

### Discussion

Salvatore Sanfilippo, the creator of Redis, is a strong proponent of a 'zero-configuration'
install philosophy. Indeed, Redis has no hard dependencies. We've even timed how long it takes
to go from "download to server interaction": 34 seconds at last check.

### See Also
