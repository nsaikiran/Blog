---
title:  "Monitoring applications"
description: "Monitoring large scale applications"
categories: ["system-design"]
date: 2024-11-21 19:45:31 +0530
author: "Sai Kiran"
comments: false
---

Application health monitoring and useful alerts are essential because we expect our services always available. I've seen a setup that has [prometheus](https://prometheus.io/) which collects metrics *exposed* from target applications (for ex: spring actuator) and [grafana](https://grafana.com/) which plots the metrics.
We can also configure alerts in these based on the result of queries on the data collected etc.

We've also used applicaiton performance monitoring from new relic. New relic is a proprietary observability platform where as above setup is open source. In new relic also we can visualize the metrics and setup alerts.

Another tool was splunk, our logs are pushed to splunk instance and where we can run queries to understand issues etc. We configured alerts here as well. We configure some query to run on a particualar interval and based on result we configure to send alerts over several channels like: email, slack etc.

We should be able to get lot of blogs explaining how to configure the setup.
