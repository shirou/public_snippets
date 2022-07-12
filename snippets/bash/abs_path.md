---
title: get abs path of script file
tags:
  - bash
---
script_dir=$(cd $(dirname ${BASH_SOURCE:-$0}); pwd)
