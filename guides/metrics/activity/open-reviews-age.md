# \# Open reviews age

Since when they are created the PRs/MRs that are currently open.

```
index: 'all'
filter: (pull_request:True or merge_request:True) and state:'open'
aggregation: 'date_histogram', field: 'created_at', calendar_interval: '1w'
```
