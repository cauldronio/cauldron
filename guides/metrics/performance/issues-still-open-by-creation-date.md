# \# Issues still open by creation date

This visualization shows the currently open issues, grouped by their creation date.

```
index: 'all'
filter: pull_request=False or is_gitlab_issue=1
aggregation: 'date_histogram', field='created_at', calendar_interval='1M'
```
