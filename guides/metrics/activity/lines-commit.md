# \# Lines/commit

Average lines changed per commit, ignoring pull/merge request commits.
- Last month: from 1 month ago to now.
- Last year: from 1 year ago to now.
- Year-over-year: comparison of lines/commit from last year to the previous year.

```
index: 'git'
average: 'lines_changed'
range: from_date < 'grimoire_creation_date' < to_date
filter: 'terms', origin=urls
filter: 'files' is not 0
```
