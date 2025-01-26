---
layout: post
title:  "Event driven systems"
description: "How event driven architecture works"
categories: ["system-design"]
date: 2025-01-26 19:45:31 +0530
author: "Sai Kiran"
comments: false
---

I was reading about the _event driven architecture_. The usecases of it, how it is used in current software systems and its benefits. Major tools for event driven architecture are Apache kafka, Rabbit MQ and Amazon SQS.

THe below resources help to understand usecases where event driven architecture fits (and kafka)

* [Apache kafka usecases](https://www.youtube.com/watch?v=BsojaA1XnpM&list=PLa7VYi0yPIH2PelhRHoFR5iQgflg-y6JA&index=3)
* [What is kafka](https://www.youtube.com/watch?v=aj9CDZm0Glc)
* [Fundamentsl of kafka](https://www.youtube.com/watch?v=B5j3uNBH8X4&list=PLa7VYi0yPIH2PelhRHoFR5iQgflg-y6JA&index=3)

I think the movitation for event driven architecture is that, we recognize and event (about some model/object). In current time, software systems are dealing of lot of events. There are so many posts in social networks, lot of retail traffic, so many financial transactions etc. All these are required to be processed in real time. Another important point is that event driven architecture decouples serveral subsystems for abstracting out details/ease scaling of subsystems (microservices).
For clear explanation of these usecases refer above videos.

TODO: Know the strengths of kafka, amazon sqs, and rabbit mq.

Event driven architecture is used with below patterns:
[Event sourcing](https://microservices.io/patterns/data/event-sourcing.html#solution) and systems using MQTT protocol to collect lightweight telemetry data.

Event sourcing is stream of events on an object/model and to arrive at current state of the object you just have to apply all the events in the order. The usecases maybe where you want to have strict audit what's going on. MQTT is a lightweight protocol used in IoT which collect lot of events, and we forward those events to kafka topics for further processing/analysis/persistence.

Also, came across, [CQRS pattern](https://www.geeksforgeeks.org/cqrs-command-query-responsibility-segregation/): where we cleraly segregate the write and read models on a system. One basic usecase can be you want to have a seperate database replica to server reads and have writes/updates done on actual database.
