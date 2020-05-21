# fzql
Fuzzily full-text search an sqlite database

## What it does:
Pipes sqlite3's output to fzf and take advantage of fzf's ability to fuzzy search the results.

## Advantages over sqlite3's excellent FTS virtual tables:
* No need to have the FTS tables established, just perform an ad-hoc full-text search on query results
* Perform a fuzzy search

## Dependencies:
1. [fzf] (https://github.com/junegunn/fzf)
2. [sqlite3] (https://sqlite.org)

## Example:
```bash
fzql my_database "select * from my_table;"
```
