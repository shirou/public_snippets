---
description: a file exists or not
tags:
  - python
---
from pathlib import Path

fpath = Path('${1:filepath}') 
if fpath.is_file(): 
    pass
