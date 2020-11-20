# \# Reviews created (chart)

Number of reviews created along the time.

```
index: 'all'
range: from_date < 'created_at' < to_date
filter: pull_request:True or merge_request:True
aggregation: 'date_histogram', field:'created_at', calendar_interval:'1w'
```
