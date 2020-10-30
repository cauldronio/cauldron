# Reviews created / closed ratio

This visualization shows the ratio between reviews created and closed in a given period.

```
index: 'all'
filter: (pull_request=True or merge_request=True) and state=['open', 'opened']
aggregation: 'range', 'created_at'={'gte': from_date, "lte": to_date}
             'date_histogram', field='created_at', calendar_interval=interval_elastic
aggregation: 'range', 'closed_at'={'gte': from_date, "lte": to_date}
             'date_histogram', field='closed_at', calendar_interval=interval_elastic
```
