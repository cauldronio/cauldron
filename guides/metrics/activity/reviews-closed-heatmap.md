# Reviews Closed Heatmap

Number of PRs/MRs closed (and merged) by weekday and by day time in the period defined by the user.

## Elasticsearch query parameters
```
index: 'all'
filter: pull_request:True or merge_request:True
filter: 'terms', origin=urls
<closed>
    aggregation: 'filter': range(from_date < closed_at < to_date)
    aggregation: 'terms', script: "doc['closed_at'].value.dayOfWeek", size:7, order={'_term': 'asc'}
    aggregation: 'terms', script: "doc['closed_at'].value.getHourOfDay()", size:24, order={'_term': 'asc'}
<merged>
    aggregation: 'filter': range(from_date < merged_at < to_date)
    aggregation: 'terms', script: "doc['merged_at'].value.dayOfWeek", size:7, order={'_term': 'asc'}
    aggregation: 'terms', script: "doc['merged_at'].value.getHourOfDay()", size:24, order={'_term': 'asc'}
```
