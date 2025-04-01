# QuestDB Command Line Shell With Keyword and Table Name Auto-Completion

Web Console is nice, but I miss the terminal -   
Write up and demo: https://teddysc.me/blog/rlwrap-questdb-shell

See also `questdb-rest` that provides the CLI this shell depends on:
- Write up and demo: https://teddysc.me/blog/questdb-rest
- GitHub: https://github.com/tddschn/questdb-rest
- PyPI: https://pypi.org/project/questdb-rest/

## Installation

- Install rlwrap with your package manager, for Homebrew it's `brew install rlwrap`
- `pipx install questdb-shell && qdb-cli gen-config`, edit the config if your db instance is not running on `localhost:9000` ([doc](https://github.com/tddschn/questdb-rest))
- Clone this repo and copy `questdb-shell` to your `$PATH`

Then run `questdb-shell` to start the shell, and test with `tables` query to see if it works.

## Screenshots

![CleanShot-2025-03-31-18.00.21_base64.png](https://g.teddysc.me/tddschn/e5bb610d28e63f5f81ec2c5f70dbda3b/CleanShot-2025-03-31-18.00.21_base64.png?b)
![CleanShot-2025-03-31-18.10.16_base64.png](https://g.teddysc.me/tddschn/e5bb610d28e63f5f81ec2c5f70dbda3b/CleanShot-2025-03-31-18.10.16_base64.png?b)


2nd screenshot shows autocompletion of both table names and SQL keywords. The `chhist_*` tables stores my chrome history dump for further analysis 🙃.


## Demo (1 min)

I use tab to trigger completion auggestions of table names and [SQL keywords](https://github.com/questdb/sql-grammar).

Half way through the demo, I accidentally made a query that returned 10 million rows (the `equities_1d` table), and I had to `Control-Z` to put the process in the background (since it wasn't responding to `Control-C`) and killed it with `kill %1` 😊.

https://www.youtube.com/watch?v=Z_36FI_DDDQ