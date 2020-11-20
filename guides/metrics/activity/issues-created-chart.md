# \# Issues created (chart)

Number of issues created along the time.

```
index: 'all'
range: from_date < 'created_at' < to_date
filter: pull_request:False or is_gitlab_issue:1
aggregation: 'date_histogram', field:'created_at', calendar_interval:'1w'
```
