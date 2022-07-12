---
title: list process
tags:
  - sql
  - postgres
---
SELECT 
    pid, backend_start, now()- backend_start as backend_duration, query_start, now()- query_start as query_duration, wait_event_ty
pe, wait_event, state,  query 
FROM pg_stat_activity WHERE pid <> pg_backend_pid() order by pid;
