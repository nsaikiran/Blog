---
layout: post
title:  "Store weak pointer to self"
description: "weak pointer to self: c++ smart pointer"
categories: ["c++"]
date: 2023-12-11 19:45:31 +0530
author: "Sai Kiran"
comments: false
---

Was going through https://itecnote.com/tecnote/c-store-weak-pointer-to-self/ and then came to know that [we can have a weak pointer to self](https://en.cppreference.com/w/cpp/memory/enable_shared_from_this).
This technique can be used to make sure everyone is using the same object, kind of like a singleton.
