# Public Snippets

This repository collects and publishes various snippets.


## Directory structure

```
.
├── README.md
├── snippets
│   ├── docker
│   ├── git
│   ├── typescript
│   ├── unix
│   │   └── ntp
│   └── zfs
└── tools    
```

- Snippets should be placed under `snippets` directory.
- Directories can be nested.
- `tools` directory will contain some converter tools.

### Languages

Directory which is related to computer languages might be placed on first level under snippets. The directory name should be same as `ace_mode` in [GitHub supported languages](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml).


## Snippets format

Each snippet is written in markdown. We may define the following three types of frontmatter. All of them are optional.

- `title`: title
- `description`: description
- `tags`: tag

Snippets itself is written in a body part.

### Placeholder

`${1:envname}` or `${2:foo}` ara placeholders.  You can use those if your editor can handle those.

### Example

```
---
title: file exists
description: a file exists or not
tags:
  - python
---
from pathlib import Path

fpath = Path('${1:filepath}')
if fpath.is_file():
    pass
```

# Contribution

Always welcome. But please agree to the license.

# License

Apache License 2.0
