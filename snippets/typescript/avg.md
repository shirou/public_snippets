---
title: avg
tags:
  - typescript
---
const avg = (...nums: Array<number>) => nums.reduce((a, b) => a + b, 0) / nums.length;
