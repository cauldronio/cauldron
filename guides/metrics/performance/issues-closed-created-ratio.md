# Issues closed / created ratio

This visualization shows the ratio between issues closed and created in a given period.

```
index: 'all'
filter: (pull_request=False or is_gitlab_issue=1) and state=['open', 'opened']
filter: 'terms', origin=urls
aggregation: 'range', 'created_at'={'gte': from_date, "lte": to_date}
             'date_histogram', field='created_at', calendar_interval=interval_elastic
aggregation: 'range', 'closed_at'={'gte': from_date, "lte": to_date}
             'date_histogram', field='closed_at', calendar_interval=interval_elastic
```
