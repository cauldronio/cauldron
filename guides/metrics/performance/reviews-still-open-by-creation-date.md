# \# Reviews still open by creation date

This visualization shows the currently open reviews, grouped by their creation date.

```
index: 'all'
filter: pull_request=True or merge_request=True
aggregation: 'date_histogram', field='created_at', calendar_interval='1M'
```
