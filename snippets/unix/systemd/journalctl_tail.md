---
description: journalctl with watching
tags:
  - systemd
---
journalctl -u ${1:service} -f
