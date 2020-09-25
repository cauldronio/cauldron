# \# Reviews closed by weekday

Get when the PRs/MRs are closed by weekday in the period defined by the user.

```
index: 'all'
filter: pull_request:True or merge_request:True
range: from_date < 'closed_at' < to_date
aggregation: 'terms', script: "doc['closed_at'].value.dayOfWeek"
```
