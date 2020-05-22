# fzql
Fuzzily full-text search an sqlite database

## What it does:
Simple bash script which pipes sqlite3's output to fzf and takes advantage of fzf's ability to fuzzy search the results.

## Advantages over sqlite3's excellent FTS virtual tables:
* No need to have the FTS tables established, just perform an ad-hoc full-text search on query results
* Perform a fuzzy search

## Dependencies:
1. [fzf](https://github.com/junegunn/fzf)
2. [sqlite3](https://sqlite.org)
(make sure both are in your PATH)

## Example Usage:
```bash
fzql my_database "select * from my_table;"
```

## Use case: search a database of zip code information for "Springfield"
Assume we don't know all of the field names, or perhaps more than one field may contain this value
#### Step 1: Specify the database location and the query:
<img src="https://raw.githubusercontent.com/benewberg/fzql/master/pics/command.png" width=640>

#### Step 2: Enter fuzzy search information (note that the header will be shown at all times)
<img src="https://raw.githubusercontent.com/benewberg/fzql/master/pics/fuzzy_search.png" width=960>

#### Step 3: (Optional) Select multiple rows using the Tab key
<img src="https://raw.githubusercontent.com/benewberg/fzql/master/pics/multi_select.png" width=960>

#### Step 4: Hit the Enter key to display the result (note that the header will also be displayed)
<img src="https://raw.githubusercontent.com/benewberg/fzql/master/pics/result.png" width=960>
