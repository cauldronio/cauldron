# Median time to close

Median time to close issues (issues closed in the period defined by the user that were opened at any time).

```
index: 'all'
50th percentil: 'time_to_close_days'
range: from_date < 'closed_at' < to_date
filter: 'terms', origin=urls
filter: pull_request:False or is_gitlab_issue:1
filter: state:'closed'
```
