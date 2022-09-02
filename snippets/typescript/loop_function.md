---
title: loop a function
tags:
  - typescript
---
const loop = (x: number, fn: (value: any, index: number, array: any[]) => void) => [...Array(x)].forEach(fn);

loop(10, () => console.log("Hello World!"));
