# \# Issues open by weekday

Get when the issues are opened by weekday in the period defined by the user.

```
index: 'all'
filter: pull_request:False or is_gitlab_issue:1
range: from_date < 'created_at' < to_date
filter: 'terms', origin=urls
aggregation: 'terms', script: "doc['created_at'].value.dayOfWeek"
```
