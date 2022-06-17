---
title: decode secrets
description: decode secret by using jq command
tags:
  - k8s
---
kubectl get secret ${1:secret} -o json | jq '.data|map_values(@base64d)'

