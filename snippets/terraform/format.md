---
title: format manifests
description: format all manifest in current directory
tags:
  - terraform
---
ls -1 *.tf | xargs -I@ terraform fmt @
