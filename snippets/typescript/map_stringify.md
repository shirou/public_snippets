---
title: stringify on Map
description: get JSON on Map
---
const body = new Map<string, string>().set("foo", "bar");
console.log(JSON.stringify({ ...Object.fromEntries(body) }));
