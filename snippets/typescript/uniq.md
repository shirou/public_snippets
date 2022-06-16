---
description: unique string array
tags:
  - typescript
---
const uniq = (src: string[]) => {
  return src.filter((elem, index, self) => self.indexOf(elem) === index);
};
