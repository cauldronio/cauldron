# Active submitters (Issues)

Evolution of the number of active issue submitters in the period defined by the user.

```
index: 'all'
filter: pull_request:False or is_gitlab_issue:1
range: from_date < 'grimoire_creation_date' < to_date
filter: 'terms', origin=urls
aggregation: 'date_histogram', field: 'grimoire_creation_date', calendar_interval: '1w'
  unique count: 'author_uuid'
```
