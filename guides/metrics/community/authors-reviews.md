# Active submitters (PRs/MRs)

Evolution of the number of active submitters of PRs/MRs in the period defined by the user.

```
index: 'all'
filter: pull_request:True or merge_request:True
range: from_date < 'grimoire_creation_date' < to_date
filter: 'terms', origin=urls
aggregation: 'date_histogram', field: 'grimoire_creation_date', calendar_interval: '1w'
  unique count: 'author_uuid'
```
