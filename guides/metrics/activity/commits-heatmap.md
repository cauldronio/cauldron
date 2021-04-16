# \# Commits by hour and weekday (local time of commit author)

The heatmap shows what times of day contributors in their local time zone contribute. Activity that clusters between regular office hours on workdays can indicate activity by contributors who do this as part of their job. Activity during evenings and weekends can indicate volunteer activity. Exclude commits with the same hash across many repositories.

```
index: 'git'
filter: 'files' is not 0
range: from_date < 'grimoire_creation_date' < to_date
filter: 'terms', origin=urls
aggregation: 'terms', field:'commit_date_weekday', size:7, order={'_term': 'asc'}
aggregation: 'terms', field:'commit_date_hour', size:24, order={'_term': 'asc'}
aggregation: 'cardinality', field: 'hash'
```
