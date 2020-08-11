# \# Issues open by weekday

Get when the issues are opened by weekday.

```
index: 'git'
filter: (pull_request:False or is_gitlab_issue:1)
aggregation: 'terms', script: "doc['created_at'].value.dayOfWeek"
```
