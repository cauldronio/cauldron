# \# Reviews closed (chart)

Number of reviews closed along the time.

## Elasticsearch query parameters
```
index: 'all'
filter: pull_request:True or merge_request:True
extra: size=0
<closed>
    aggregation: 'filter': range(from_date < closed_at < to_date)
    aggregation: 'date_histogram', field: 'closed_at', calendar_interval: '1w'
<merged>
    aggregation: 'filter': range(from_date < merged_at < to_date)
    aggregation: 'date_histogram', field: 'merged_at', calendar_interval: '1w'
```
