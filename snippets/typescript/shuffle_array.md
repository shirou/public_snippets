---
title: shuffle array
tags:
  - typescript
---
const shuffleArray = (array: Array<unknown>) => array.sort(() => Math.random() - 0.5);
