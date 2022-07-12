---
title: find lock table
tags:
  - sql
  - postgres
---
select nspname,relname,l.* from pg_locks l join pg_class c on
 (relation=c.oid) join pg_namespace nsp on (c.relnamespace=nsp.oid) where
  pid in (select pid from pg_stat_activity where
  datname=current_database() and query!=current_query());
