# \# Reviews closed (chart)

Number of reviews closed along the time.

```
index: 'all'
range: from_date < 'closed_at' < to_date
filter: pull_request:True or merge_request:True
aggregation: 'date_histogram', field:'closed_at', calendar_interval:'1w'
```
