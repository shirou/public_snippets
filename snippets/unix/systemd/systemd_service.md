---
description: systemd simple service
tags:
  - systemd
---
[Unit]
Description=${1:desc}

[Service]
Type=simple
ExecStart=${2:fullpath}

[Install]
WantedBy=multi-user.target
