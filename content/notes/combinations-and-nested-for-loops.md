---
title:  "Combinations"
description: "Generating all k-combinations of "
categories: ["algorithms"]
date: 2023-12-11 19:45:31 +0530
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
