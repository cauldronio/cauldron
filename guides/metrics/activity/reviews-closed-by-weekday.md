# \# Reviews closed by weekday

Get when the PRs/MRs are closed by weekday in the period defined by the user.

## Elasticsearch query parameters
```
index: 'all'
filter: pull_request:True or merge_request:True
filter: 'terms', origin=urls
extra: size=0
<closed>
    aggregation: 'filter': range(from_date < closed_at < to_date)
    aggregation: 'terms', script: "doc['closed_at'].value.dayOfWeek"
<merged>
    aggregation: 'filter': range(from_date < merged_at < to_date)
    aggregation: 'terms', script: "doc['merged_at'].value.dayOfWeek"
```
