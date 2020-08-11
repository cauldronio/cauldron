# \# Reviews open by weekday

Get when the PRs/MRs are opened by weekday.

```
index: 'git'
filter: pull_request:True or merge_request:True
aggregation: 'terms', script: "doc['created_at'].value.dayOfWeek"
```
