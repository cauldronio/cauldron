# \# Authors of commits

Evolution of the number of commits authors in the period defined by the user, ignoring pull/merge request commits.

```
index: 'git'
filter: 'files' is not 0
range: from_date < 'grimoire_creation_date' < to_date
aggregation: 'date_histogram', field: 'grimoire_creation_date', calendar_interval: '1w'
  unique count: 'author_uuid'
```
