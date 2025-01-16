---
layout: post
title:  "Connection pooling"
description: "Better resource management, reduce the overhead on server"
categories: ["connection-pool"]
date: 2023-12-11 19:45:31 +0530
author: "Sai kiran"
comments: false
---

At first, when I read about connection polling, they say it is used for proper resource management, performance and scalability. 

Why connection pooling is beneficial? No. of connections created on machine is limited (as the resources in machine are limited), opening a new connection is costly with respect to time. And some software like Postgres and Apache has process based model, meaning, for each connection they may spawn a new process to serve, if the number of simultaneous connections are increasing then it'll put lot of pressure on resources.

Hence, you'll use connection pooling or connection manager etc, that holds a fixed number of connections and those connections will be shared and reused.

Know more about how connection managers work, how clients use connection manager etc.

Watch [PostgreSQL connection management and per-client process model explained](https://www.youtube.com/watch?v=o7qLKfILuD8)

Connection pooling:

- [HikariCP - About pool sizing](https://github.com/brettwooldridge/HikariCP/wiki/About-Pool-Sizing)
- [Real-World Performance - 13 - Large Dynamic Connection Pools - Part 1](https://www.youtube.com/watch?v=Oo-tBpVewP4)
- [Real-World Performance - 14 - Large Dynamic Connection Pools - Part 2](https://www.youtube.com/watch?v=XzN8Rp6glEo)
- old video [OLTP Performance - Concurrent Mid-Tier Connections](https://www.youtube.com/watch?v=xNDnVOCdvQ0)

Even from HTTP/1.1 connections to the webservers are reused by using keep-alive header

How nginx handles many connections simultaneously.

- [How Does NGINX Work?](https://www.nginx.com/blog/inside-nginx-how-we-designed-for-performance-scale/#process-model) read the comments.
They are very informative.
- [Socket sharding nginx](https://www.nginx.com/blog/socket-sharding-nginx-release-1-9-1/)

### Summary

Learn about connection polling in general with various examples.