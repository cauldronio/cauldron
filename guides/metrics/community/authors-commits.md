# Active authors (Git)

Evolution of the number of active commit authors in the period defined by the user, ignoring pull/merge request commits.

```
index: 'git'
filter: 'files' is not 0
range: from_date < 'grimoire_creation_date' < to_date
filter: 'terms', origin=urls
aggregation: 'date_histogram', field: 'grimoire_creation_date', calendar_interval: '1w'
  unique count: 'author_uuid'
```
