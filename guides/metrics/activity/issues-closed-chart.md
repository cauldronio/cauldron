# \# Issues closed (chart)

Number of issues closed along the time.

```
index: 'all'
range: from_date < 'closed_at' < to_date
filter: pull_request:False or is_gitlab_issue:1
aggregation: 'date_histogram', field:'closed_at', calendar_interval:'1w'
```
