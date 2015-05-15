<!--
name: make-data-more-durable
freshnessDate: 2014-12-04
version : "0.9"
title : "Make Data in Redis More Durable With The Append-Only File"
description: "Part of the Redis Cookbook, http://www.rediscookbook.org"
homepage : "http://www.rediscookbook.org"
author : "Ted Nyman"
license : "CC Attribution Share Alike 3.0"
-->

<!-- @section -->

### Problem

You want to increase the durability of your data in Redis.

### Solution

Use Redis' built-in *append-only file* (AOF).

Edit the Redis configuration file `redis.conf` to include the line:
	appendonly yes

Redis will now add every command to the AOF. If the server should crash, you will be able to
rebuild state from this file. It works in a very similar fashion to the log files common in
other databases, such as MySQL's binlog.

### Discussion

The AOF itself is configurable. There are three different options, each with their own particular
tradeoff between durability and speed. These configurations can be set in `redis.conf`.

The three options are to force a sync every command, sync every second, or never force a sync (that is, leave the process up to the operating system). Redis' default is the sync on every command; however, this will be quite slow. The second option is usually a fair trade-off between safety and speed.

### See Also


