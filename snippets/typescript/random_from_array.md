---
title: random from array
tags:
  - typescript
---
const getRandomElement = (array: Array<unknown>) => array[~~(Math.random() * array.length)];
