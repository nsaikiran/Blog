---
title:  "N-choose-K"
description: "Generating all k-combinations of N objects using nested for loops"
categories: ["algorithms"]
date: 2024-05-28 19:45:31 +0530
author: "Sai kiran"
comments: false
---

Given N objects, and we want to choose some K objects. How many such K-combinations we can generate. Assuming each object is unique. While solving problems we often need to generate combinations. For example: Given an array of numbers find any pair of numbers whose sum equals to P. 0-1 knapsack problem in which we are supposed to fill the knapsack with a fixed capacity by maximinzing the value of objects selected.

One way we can generate the combinations is using nested for-loops. 

```#Generate combinations of N-choose-2
for i in range(len(N) - 1):
    for j in range(i+1, len(N)):
        (i, j) #combination
```

How does this generate the correct result? Why the inner loop starts from `i`?
The outer loop fixes one element and inner loop goes over all remaining elements, such that the pair never repeats. If the inner loop also starts from the beginning of the list, then we will see the combinations that we have already seen.
Remember the difference between combinations and permutations. Here we are looking for combinations.
What is the time complexity here?
```n-1 + n-2 + n-3 + ... + 1 ```
This is same as sum of first n-1 natural numbers, refer [here](https://en.wikipedia.org/wiki/1_%2B_2_%2B_3_%2B_4_%2B_%E2%8B%AF). ~ O(n^2)

------

Incase if we need to generate all N-choose-k where k = 3 (above scenario is k=2)

```#Generate combinations of N-choose-2
for i in range(len(N) - 2):
    for j in range(i+1, len(N) - 1):
        for k in range (j+1, len(N)):
            (i, j, k) #combination
```