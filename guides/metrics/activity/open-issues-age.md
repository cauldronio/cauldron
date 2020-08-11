# \# Open issues age

Since when they are created the issues that are currently open.

```
index: 'all'
filter: (pull_request:False or is_gitlab_issue:1) and state:'open'
aggregation: 'date_histogram', field: 'created_at', calendar_interval: '1w'
```
