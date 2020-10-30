# Time to close (Issues created)

This visualization shows the average and the median time to close of created issues in a given period.

```
index: 'all'
filter: pull_request=False or is_gitlab_issue=1
filter: created_at={'gte': from_date, "lte": to_date}
aggregation: 'date_histogram', field='created_at', calendar_interval=interval_elastic
             metric: 'avg', field='time_to_close_days'
             metric: 'percentiles', field='time_to_close_days', percents=[50]
```
