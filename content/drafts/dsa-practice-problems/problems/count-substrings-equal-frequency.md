---
layout: post
title:  "Count Substrings with Equal Frequency"
description: "DSA"
categories: ["tech", "cs"]
tags: ["algorithms"]
date: 2023-12-12 19:45:31 +0530
author: "Sai Kiran"
---

## Problem

Given a string with fixed characters repeating. Find all the substrings where all the fixed characters same frequency. For ex: RRAABBBRRAARB


## Solutions

### Naive

- Generate all the substings - polynomial, by selecting the start and end index.
- Iterate over each substring, count the frequency of all characters in it: linear time
- If all characters have same count then take that as one of the result.
- O(n^3)

```python
def count_valid_substrings(s):
    n = len(s)
    valid_count = 0
    
    # Iterate over all possible substrings
    for i in range(n):
        freq = {}
        for j in range(i, n):
            # Add current character to frequency dictionary
            char = s[j]
            if char in freq:
                freq[char] += 1
            else:
                freq[char] = 1
            
            # Check if all characters have the same frequency
            if len(set(freq.values())) == 1:
                valid_count += 1
    
    return valid_count

# Example usage:
s = "aabbcc"
print(count_valid_substrings(s))  # Output: 6

```

### Slightly optimized

```python
from collections import defaultdict

def count_valid_substrings(s):
    n = len(s)
    total_valid_substrings = 0
    
    # Iterate over each possible length for the substrings
    for i in range(n):
        freq = defaultdict(int)
        freq_count = defaultdict(int)
        distinct_chars = 0

        # Expanding the window
        for j in range(i, n):
            char = s[j]
            if freq[char] > 0:
                freq_count[freq[char]] -= 1
                if freq_count[freq[char]] == 0:
                    del freq_count[freq[char]]
            
            freq[char] += 1
            freq_count[freq[char]] += 1

            # The window is valid if there is only one unique frequency count
            if len(freq_count) == 1:
                total_valid_substrings += 1
    
    return total_valid_substrings

# Example usage:
s = "aabbcc"
print(count_valid_substrings(s))  # Output: 6
```

### Optimized
```python

from collections import defaultdict


```

[Chatgpt was able to answer this question!](https://chatgpt.com/share/eddb6200-22a3-4bf7-a128-634e7c2a2426). Need to upskill!!