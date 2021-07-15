---
layout: post
title: Selecting a database in PostgresSQL
tags: PostgresSQL
---

1. open psql `psql -U pg`
2. list databases `\list` or `\l`
3. select a database `\connect DBNAME` or `\c DBNAME`
4. list all database tables `\dt` using the `search_path`
    1. list all database tables regardless of `search_path` by `\dt *.`
    2. describe the table to see schema `\d TABLE_NAME`
    3. more info with `\d+`
5. show data `select * from TABLE`
