# \# Reviews closed by weekday

Get when the PRs/MRs are closed by weekday.

```
index: 'git'
filter: pull_request:True or merge_request:True
aggregation: 'terms', script: "doc['closed_at'].value.dayOfWeek"
```
