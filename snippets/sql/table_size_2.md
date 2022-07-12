---
title: get size of all table (another version)
tags:
  - sql
  - postgres
---
select cls.relname as table_name , cls.reltuples as row_num, (cls.relpages * 8 /1024) as table_mbyte, (cls.relpages * 8 /1024 /1024) as table_gbyte
      ,cls.relkind as object_kind -- r:table i:index S:seq v:view c:composit t:toast table
  from pg_class cls INNER JOIN pg_namespace nsp ON (cls.relnamespace = nsp.oid)
 where nsp.nspname = 'public' and cls.reltuples > 0
 order by table_mbyte desc;
