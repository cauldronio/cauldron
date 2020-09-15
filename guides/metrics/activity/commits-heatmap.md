# \# Commits by hour and weekday (local time of commit author)

Number of commits by weekday and by day time in the period defined by the user, ignoring merge request commits (at least 1 file changed).

```
index: 'git'
filter: 'files' is not 0
range: from_date < 'grimoire_creation_date' < to_date
aggregation: 'terms', field:'commit_date_weekday', size:7, order={'_term': 'asc'}
aggregation: 'terms', field:'commit_date_hour', size:24, order={'_term': 'asc'}
```
