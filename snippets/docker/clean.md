---
title: clean
description: remove image and container not been used recently. run with systemd-timer is better.
tags:
  - docker
---
docker image prune -a -f --filter "until=720h"
docker container prune -f --filter "until=48h"
