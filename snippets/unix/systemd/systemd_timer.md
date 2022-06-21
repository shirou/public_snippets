---
description: systemd simple timer
tags:
  - systemd
---
[Unit]
Description=${1:desc}

[Timer]
OnBootSec=1min  # start 1 min later from boot
OnUnitActiveSec=${2:interval}  # interval
Unit=${3:servicename}.service

[Install]
WantedBy=multi-user.target
