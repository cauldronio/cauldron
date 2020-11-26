# \# Commits

Number of commits, ignoring empty commits.
- Last month: from 1 month ago to now.
- Last year: from 1 year ago to now.
- Year-over-year: comparison of commits from last year to the previous year.

## Elasticsearch query parameters
```
index: 'git'
unique count: 'hash'
range: from_date < 'grimoire_creation_date' < to_date
filter: 'terms', origin=urls
filter: 'files' is not 0
```
