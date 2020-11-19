# \# Issues closed

Number of closed issues in a period of time
- Last month: from 1 month ago to now.
- Last year: from 1 year ago to now.
- Year-over-year: comparison of issues closed from last year to the previous year.

```
index: 'all'
range: from_date < 'closed_at' < to_date
filter: 'terms', origin=urls
filter: pull_request:False or is_gitlab_issue:1
filter: 'state' is 'closed'
```
