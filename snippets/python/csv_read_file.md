---
title: CSV file read
tags:
  - python
---
with open(fname) as csvfile:
    reader = csv.reader(csvfile)
    for row in reader:
        print(', '.join(row))
