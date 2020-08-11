# \# Issues open/closed

Open and closed issues by date in the period defined by the user.

```
index: 'all'
filter: pull_request:False or is_gitlab_issue:1
<open>
    aggregation: 'filter': range(from_date < created_at < to_date)
    aggregation: 'date_histogram', field: 'created_at', calendar_interval: '1w'
<closed>
    aggregation: 'filter': range(from_date < closed_at < to_date)
    aggregation: 'date_histogram', field: 'closed_at', calendar_interval: '1w'
```
