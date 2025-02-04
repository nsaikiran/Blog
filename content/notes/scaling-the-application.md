---
layout: post
title:  "Scaling the application"
description: "How to scale applications for increased users, load with cost effectiveness"
categories: ["system-design"]
date: 2024-03-15 19:45:31 +0530
author: "Sai Kiran"
comments: false
---

Software applications should be able to serve increased users and load with reasonable cost. The goal of the businesses have been to build highly available software with resonable opertaing cost. 

## Reading material
(This is not an exhaustive list of resources, and not in any particular order. The goal is first understand various concepts, various usecases in which these concepts can be applied and implementations of these concepts. For example: what are the load balancers, reverse proxies, web servers, caches, databases that can be used. And also, it is important to know various characteristics of our systems such as how many requests/users one node of our system can handle so that we take an informed decision)
1. [The System Design Primer](https://github.com/donnemartin/system-design-primer/blob/master/README.md) has described the general concepts that are required for scaling software systems. This guide cites very informative articles or blog posts from various industry experts.
2. [Scaling on AWS for the First 10 Million Users](https://www.youtube.com/watch?v=LbiPMKDNdvY) and [its slides](https://www.slideshare.net/AmazonWebServices/scaling-on-aws-for-the-first-10-million-users-at-websummit-dublin-41845658?from_search=9). 
   - Every year, AWS team have a presentation that talks about _Scaling Up to Your First 10 Million Users with AWS offerings_, the link I've mentioned here is the oldest I could find (I think this is from 2013), but if there is older one prefer that one, because the latest talks mentions latest AWS offerings which are very abstract. 
   - The goal here is to understand the concepts.
   - Some of the previous events are [Scaling Up to Your First 10 Million Users/2014](https://www.youtube.com/watch?v=ccojvcQq858), [Deep Dive: Scaling Up to Your First 10 Million Users / 2015](https://www.youtube.com/watch?v=KulMgJnMLsw), find the respective slides from [slideshare](https://www.slideshare.net/search?utf8=%E2%9C%93&searchfrom=header&q=+Scaling+on+AWS+for+the+First+10+Million+Users+). Compare the slides to learn differences.
3. [It's all a numbers game](https://www.youtube.com/watch?v=1KRYH75wgy4) Try to get the numbers for the system by having clear understanding, numbers don't lie and they'll give a chance to unambiguous and informed scaling decision.
4. [Baseds](https://medium.com/baseds) by Vaidehi

Go through these and list down concepts and describe those concepts.

## Important links to go through
- [What is ..aaS?](https://web.archive.org/web/20190327064546/http://www.lecloud.net/post/11380869305/what-is-aas)
- [AWS Elasticity](https://wa.aws.amazon.com/wat.concept.elasticity.en.html)
- [REST](https://restcookbook.com/Basics/hateoas/)
- [Debug the How do you debug a distributed system]( https://www.linkedin.com/advice/0/how-do-you-debug-distributed-system-multiple)
- [Applying Back Pressure When Overloaded](https://mechanical-sympathy.blogspot.com/2012/05/apply-back-pressure-when-overloaded.html)
- [Overview of Single vs. Multi Server Architecture](https://lethain.com/overview-of-single-vs-multi-server-architecture/) and [Measuring Single and Multi Server Performance](https://lethain.com/measuring-server-performance-single-vs-multi/)
- [Google Architecture](https://highscalability.com/google-architecture/)
- [Google File system](https://research.google/pubs/the-google-file-system/)
- [Introduction to Microservices]( https://www.nginx.com/blog/introduction-to-microservices/)
- [Webinar 2012: 7 Steps to Select the Right Architecture for Your Web Application on AWS](https://www.youtube.com/watch?v=Ypwi1Ics91Y)
### Read these and keep or delete from here
#### Session/cookies
- [Internet Cookies: Types, Function, and Alternatives](https://timesinternet.in/blog/types-of-internet-cookies-and-their-alternatives/)
- [What Is Session Persistence?](https://www.nginx.com/resources/glossary/session-persistence/)
- [Getting Rid of Sticky Sessions in Java](https://www.couchbase.com/blog/sticky-sessions/)
#### CSR vs SSR
- [Server-Side Rendering: Everything You Need to Know]( https://www.cloudbees.com/blog/server-side-rendering)
- [SSR in Node.js](https://blog.bitsrc.io/demystifying-server-side-rendering-lets-build-our-own-ssr-server-with-node-js-c88c6c1e949d)
- When to use SSR vs CSR
#### Hashing
- [Consistent Hashing]( https://www.paperplanes.de/2011/12/9/the-magic-of-consistent-hashing.html)
#### Elastic search
- [Elasticsearch from the Bottom Up](https://www.elastic.co/blog/found-elasticsearch-from-the-bottom-up)
#### RDMS
- [Denormalization in Databases: Pros, Cons, and Techniques](https://blog.invgate.com/denormalization-in-databases)
#### Misc
- [Scaling on AWS for the First 10 Million Users at Websummit Dublin](https://www.slideshare.net/AmazonWebServices/scaling-on-aws-for-the-first-10-million-users-at-websummit-dublin-41845658?from_search=9)
