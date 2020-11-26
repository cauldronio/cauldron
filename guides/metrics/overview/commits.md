# \# Commits

Number of commits, ignoring empty commits.

## Elasticsearch query parameters
```
index: 'git'
unique count: 'hash'
range: from_date < 'grimoire_creation_date' < to_date
filter: 'terms', origin=urls
filter: 'files' is not 0
```
