---
title: remove item
desc: remove item from list, by an index
tags:
  - golang
---
items = append(items[:i], items[i+1:]...)
