---
title: chunk array
tags:
  - typescript
---
const chunkArray = (array: Array<unknown>, chunkSize: number) =>
	[...Array(Math.ceil(array.length / chunkSize))].map((_, index) =>
		array.slice(index * chunkSize, (index + 1) * chunkSize)
	);
