# \# Reviews open by weekday

Get when the PRs/MRs are opened by weekday in the period defined by the user.

```
index: 'all'
filter: pull_request:True or merge_request:True
range: from_date < 'created_at' < to_date
filter: 'terms', origin=urls
aggregation: 'terms', script: "doc['created_at'].value.dayOfWeek"
```
