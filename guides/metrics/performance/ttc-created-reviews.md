# Time to close (Reviews created)

This visualization shows the average and the median time to close of created reviews in a given period.

```
index: 'all'
filter: pull_request=True or merge_request=True
filter: created_at={'gte': from_date, "lte": to_date}
aggregation: 'date_histogram', field='created_at', calendar_interval=interval_elastic
             metric: 'avg', field='time_to_close_days'
             metric: 'percentiles', field='time_to_close_days', percents=[50]
```
