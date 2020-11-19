# Reviews Opened Heatmap

Number of PRs/MRs opened by weekday and by day time in the period defined by the user.

```
index: 'all'
filter: pull_request:True or merge_request:True
range: from_date < 'created_at' < to_date
filter: 'terms', origin=urls
aggregation: 'terms', script: "doc['created_at'].value.dayOfWeek", size:7, order={'_term': 'asc'}
aggregation: 'terms', script: "doc['created_at'].value.getHourOfDay()", size:24, order={'_term': 'asc'}
```
