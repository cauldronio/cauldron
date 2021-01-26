# Reviews closed / created ratio

This visualization shows the ratio between reviews closed (and merged) and created in a given period.

## Elasticsearch query parameters
```
index: 'all'
filter: pull_request:True or merge_request:True
filter: 'terms', origin=urls
extra: size=0
<open>
    aggregation: 'filter': range(from_date < created_at < to_date)
    aggregation: 'date_histogram', field: 'created_at', calendar_interval: '1w'
<closed>
    aggregation: 'filter': range(from_date < closed_at < to_date)
    aggregation: 'date_histogram', field: 'closed_at', calendar_interval: '1w'
<merged>
    aggregation: 'filter': range(from_date < merged_at < to_date)
    aggregation: 'date_histogram', field: 'merged_at', calendar_interval: '1w'
```
