---
title: Sort a List of Dictionaries
tags:
  - python
---
dicts_lists = [
  {
    "Name": "James",
    "Age": 20,
  },
  {
     "Name": "May",
     "Age": 14,
  },
  {
    "Name": "Katy",
    "Age": 23,
  }
]

dicts_lists.sort(key=lambda item: item.get("Age"))
