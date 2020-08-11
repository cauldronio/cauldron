# \# Issues closed by weekday

Get when the issues are closed by weekday.

```
index: 'git'
filter: (pull_request:False or is_gitlab_issue:1)
aggregation: 'terms', script: "doc['closed_at'].value.dayOfWeek"
```
