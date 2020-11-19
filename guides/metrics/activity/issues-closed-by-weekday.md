# \# Issues closed by weekday

Get when the issues are closed by weekday in the period defined by the user.

```
index: 'all'
filter: pull_request:False or is_gitlab_issue:1
range: from_date < 'closed_at' < to_date
filter: 'terms', origin=urls
aggregation: 'terms', script: "doc['closed_at'].value.dayOfWeek"
```
