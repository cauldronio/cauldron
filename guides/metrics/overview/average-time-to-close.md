# Average time to close

Average time to close issues in a period of time (only issues closed in the time range).

```
index: 'all'
average: 'time_to_close_days'
range: from_date < 'closed_at' < to_date
filter: pull_request:False or is_gitlab_issue:1
filter: state:'closed'
```
