---
title: Remove merged branches
tags:
  - git
---
git branch --merged | grep -v master | grep -v '*' | xargs -I % git branch -d %
