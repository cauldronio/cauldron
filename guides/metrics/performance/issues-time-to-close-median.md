# Time to close (median) - Issues

This metric shows the median time to close for closed issues in a given period.

```
index: 'all'
filter: pull_request=False or is_gitlab_issue=1
filter: closed_at={'gte': from_date, "lte": to_date}
aggregation: 'percentiles', field='time_to_close_days', percents=[50]
```
