---
title: rgb to hex
tags:
  - typescript
---
const rgbToHex = (r:number, g:number, b:number) =>
	"#" + ((r << 16) + (g << 8) + b).toString(16).padStart(6, "0");
