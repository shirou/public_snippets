---
title: convert number to word
tags:
  - typescript
---
const numToWord = (num: number) =>
    num.toLocaleString("en-US", { notation: "compact" } as Intl.NumberFormatOptions);
