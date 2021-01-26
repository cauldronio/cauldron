# Time to close (median) - Reviews

This metric shows the median time to close for closed (and merged) reviews in a given period.

## Elasticsearch query parameters
```
index: 'all'
filter: pull_request=True or merge_request=True
filter: 'terms', origin=urls
range: (from_date < 'closed_at' < to_date) | (from_date < 'merged_at' < to_date)
aggregation: 'percentiles', field='time_to_close_days', percents=[50]
```
