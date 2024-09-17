---
layout: post
title:  "Reading system design"
description: "DSA"
categories: ["tech", "cs"]
tags: ["system design"]
date: 2024-08-21 19:45:31 +0530
author: "Sai Kiran"
---
## High level or large scale system design

### Collaborative software systems

[Operational transformation](https://en.wikipedia.org/wiki/Operational_transformation) is one of the core ideas behind Google Docs etc. Go through this technique. Operational transformation is like a version control system that carefully merges the changes from various operational transforms or tiny instructions that need to be applied on a doc in real time.

### Preprocessing and asynchronous processing

Always think, in the given usecase, if we can achieve better results by doing a *onetime* pre-processing of input data or serving requests *asynchronously*. These patterns sometimes give better user experience.

### Reliability, constant work

In general [All Things Distributed](https://www.allthingsdistributed.com/) is good resource.

1. [A Word on Scalability](https://www.allthingsdistributed.com/2006/03/a_word_on_scalability.html) 
2. [Reliability, constant work](https://aws.amazon.com/builders-library/reliability-and-constant-work/) explains *constant work* pattern that is suitable in some cases, which gives *anti-fragility* on high load.
    * [Always keep smaller services in control][smaller-service-in-control]

3. List goes on

## Low-level design or object oriented design questions

### Questions I've created

* Design a music player. Given some location in drive that contains music files, create a music player that has play, pause, previous, next, forward, backward, playlists creation and browsing etc.

* Design a browser tab's history tracker. Simulate back and forward button. Also, if I traverse back and move forward, we want to remember the previous next also. Basically from one state I should have multiple outgoing links.
  * Solution will stack based implementation for traversing back, each node _can_ have more than one outgoing link. Traversing back on stack datastructure is like _backtracking_ (pop operation), hence for _backtracking_ in recursion and graphs we use stack datastructure. Directory traversal is also a similar solution.

[smaller-service-in-control]: https://aws.amazon.com/builders-library/avoiding-overload-in-distributed-systems-by-putting-the-smaller-service-in-control