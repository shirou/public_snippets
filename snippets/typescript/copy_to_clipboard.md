---
title: copy to clipboard
tags:
  - typescript
---
const copyToClipboard = async (text: string) => navigator?.clipboard?.writeText(text);
