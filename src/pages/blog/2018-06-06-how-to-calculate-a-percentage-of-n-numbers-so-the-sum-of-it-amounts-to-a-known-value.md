---
templateKey: blog-post
title: How to calculate a percentage of n numbers so the sum of it amounts to a known value
date: 2018-06-06T18:00:00.000Z
description: Brewing with a Chemex probably seems like a complicated, time-consuming ordeal, but once you get used to the process, it becomes a soothing ritual that's worth the effort every time.
tags:
  - math
  - distribution
---
# How to calculate a percentage of n numbers so the sum of it amounts to a known value

```
ax + bx = y
x(a + b) = y
x = y / (a + b)
```

Use case:
You want to split a monthly bill between two people but you want to distribute the cost based on their income.

Let’s do some pseudo-code:
```
// salaries
susan = 1400
jim = 1100

// expenses
rent = 650

(susan * x) + (jim * x) = rent
x * (susan + jim) = rent
x = rent / (susan + jim)
x = 650 / (1400 + 1100)
x = 650 / 2500
x = 0.26

// Check result
(susan * x) + (jim * x) = rent
(1400 * 0.26) + (1100 * 0.26) = 650
364 + 286 = 650
650 = 650
```

They should both pay 26% of their salary to cover the rent.


This works with more than two subjects. Here’s an example of the formula
```
ax + bx + cx + dx = y
x(a + b + c + d) = y
x = y / (a + b + c + d)
```

The final formula is: `x = y / (a + b + c + … + n)` where:
- x -> Result in the form of a percentage.
- y -> Amount be spliced
- a … n -> Amounts for the parts that want to split the amount of  `y`


