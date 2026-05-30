## Overall Roadmap

Following the PostgreSQL official tutorial path, SQL first requires understanding tables, rows, and columns, then moves into querying, joins, aggregation, updates, and deletion. This repository is closer to LeetCode SQL practice, so the focus is query expression, joins, functions, aggregation, window functions, and subqueries.

```text
SQL = using declarative queries to extract answers from relational tables
|
+-- The central problems
|   +-- How is data organized in a database?
|   |   +-- Use tables, rows, columns, keys, and relationships to represent business objects.
|   +-- How can one table be filtered for the needed information?
|   |   +-- Use SELECT, WHERE, ORDER BY, LIMIT, and expressions.
|   +-- How can many tables and many rows be combined into one answer?
|       +-- Use JOIN, GROUP BY, subqueries, UNION, and window functions.
|
+-- Tool 1: basic querying
|   +-- SELECT / WHERE      choose columns and filter rows
|   +-- Computed fields     produce new results with expressions
|   +-- String and date functions handle text, time, and formatting
|   +-- Regex and conditional expressions handle finer matching and branching
|
+-- Tool 2: multi-table relations
|   +-- INNER / LEFT JOIN   connect tables by keys
|   +-- UNION / UNION ALL   combine multiple query results
|   +-- Subqueries          use one query as another query's condition or source
|
+-- Tool 3: aggregation and windows
    +-- Aggregate functions count, sum, avg, max, min
    +-- GROUP BY            compress rows into grouped results
    +-- HAVING              filter after grouping
    +-- Window functions    rank, accumulate, and compute within partitions without collapsing rows
```

<!-- Author : Dongsheng Deng & Liam Huang-->
<!-- Program Email: elegantlatex2e@gmail.com -->

[Homepage](https://elegantlatex.org/) | [Github](https://github.com/ElegantLaTeX/ElegantBook) | [CTAN](https://ctan.org/pkg/elegantbook) | [Download](https://github.com/ElegantLaTeX/ElegantBook/releases) | [Wiki](https://github.com/ElegantLaTeX/ElegantBook/wiki) | [Weibo](https://weibo.com/elegantlatex)

![License](https://img.shields.io/ctan/l/elegantbook.svg) ![CTAN Version](https://img.shields.io/ctan/v/elegantbook.svg) ![Github Version](https://img.shields.io/github/release/ElegantLaTeX/ElegantBook.svg) ![Repo Size](https://img.shields.io/github/repo-size/ElegantLaTeX/ElegantBook.svg)

-------

# ElegantBook: An Elegant LaTeX Template for Books

ElegantBook is designed for writing books, created by [Dongsheng Deng](https://ddswhu.me/) and [Liam Huang](https://liam.page/). Just enjoy it! If you have any questions, suggestions or bug reports, you can create issues or contact us at elegantlatex2e@gmail.com.

## Important Notes

For some reasons, __unauthorized__ pull requests are **UNACCEPTABLE** since May 20, 2019. For those who want to help revise the templates, submit issues or clone to your own repository to modify under the LPPL-1.3c.

## Acknowledgement

Thank [sikouhjw](https://github.com/sikouhjw) and [syvshc](https://github.com/syvshc) for their quick response to Github issues and continuously support work for ElegantLaTeX.

Thank ChinaTeX and [LaTeX Studio](http://www.latexstudio.net/) for their promotion.


## License

This work is released under the LaTeX Project Public License, v1.3c or later.


## Derivative Works

+ [ElegantBookdown](https://github.com/XiangyunHuang/ElegantBookdown)：[XiangyunHuang](https://github.com/XiangyunHuang) developed a Bookdown template based on ElegantBook.
+ [bookdownplus](https://github.com/pzhaonet/bookdownplus): maintained by [pzhaonet](https://github.com/pzhaonet).
+ [PanBook](https://github.com/annProg/PanBook)：a markdown-based writing workflow Developed by [annProg](https://github.com/annProg).
