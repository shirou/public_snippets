---
title: unique by using set
tags:
  - typescript
---
const uniqueArray = (array: Iterable<unknown> | null | undefined) => [...new Set(array)];
