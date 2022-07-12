---
title: kill process
tags:
  - sql
  - postgres
---
SELECT pg_terminate_backend(pid)
  jFROM pg_stat_activity
WHERE datname = '${0:table_name}'
  AND pid <> pg_backend_pid();
