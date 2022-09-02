---
title: random number
tags:
  - typescript
---
const getRandomNumber = (min: number, max: number) => ~~(Math.random() * (max - min + 1)) + min;
