---
title: detect dark mode
tags:
  - typescript
---
const isDarkMode = () => globalThis.matchMedia?.("(prefers-color-scheme:dark)").matches ?? false;
