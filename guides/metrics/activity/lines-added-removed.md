# \# Lines added vs removed

Number of lines added vs removed in the period defined by the user.

```
index: 'git'
range: from_date < 'grimoire_creation_date' < to_date
filter: 'terms', origin=urls
aggregation: 'date_histogram', field: 'grimoire_creation_date', calendar_interval: '1w'
aggregation: 'sum', script: "doc['lines_removed'].value * -1"
aggregation: 'sum', field: 'lines_added'
```
