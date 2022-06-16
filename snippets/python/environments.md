---
title: environment
description: get value from environment with boolean convert
tags:
  - python
---
import os
from distutils.util import strtobool

${1:envname} = strtobool(os.environ['${1:envname}']) if '${1:envname}' in os.environ else False
