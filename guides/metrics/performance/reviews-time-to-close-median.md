# Time to close (median) - Reviews

This metric shows the median time to close for closed reviews in a given period.

```
index: 'all'
filter: pull_request=True or merge_request=True
filter: closed_at={'gte': from_date, "lte": to_date}
aggregation: 'percentiles', field='time_to_close_days', percents=[50]
```
