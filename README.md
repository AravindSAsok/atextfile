# SQL Scratchpad

A small personal SQL notes repository containing an example ALTER TABLE statement and working notes. This is a scratchpad, not a deployable database migration or a complete application.

## Current SQL note

The file alter queries.txt contains an example that adds four columns to an existing accounts table:

~~~sql
ALTER TABLE accounts
  ADD user_type VARCHAR(100) NOT NULL DEFAULT 'user',
  ADD isComplete BOOLEAN NOT NULL DEFAULT true,
  ADD steps INTEGER NOT NULL DEFAULT 1,
  ADD secondary_email VARCHAR(100);
~~~

## Before using this query

- Confirm the SQL dialect and database version support this ALTER TABLE syntax.
- Inspect the existing accounts schema and check whether these columns already exist.
- Back up important data before applying schema changes.
- Review whether NOT NULL defaults are appropriate for existing rows.
- Prefer a versioned migration with a rollback plan in a real application.

The remaining lines in the original text file are informal branch and scratch notes, not executable SQL.

## Maintainer

[Aravind S Asok](https://github.com/AravindSAsok)
