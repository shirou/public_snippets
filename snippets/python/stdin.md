---
title: read from stdin
tags:
  - python
---
import sys

for line in sys.stdin:
    print(line.strip())
