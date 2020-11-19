# Median review duration

Median time to merge a pull request or merge request (reviews merged in the period defined by the user that were opened at any time)

```
index: 'all'
50th percentil: 'time_to_close_days'
range: from_date < 'grimoire_creation_date' < to_date
filter: 'terms', origin=urls
filter: (pull_request:True and state:'closed') or (merge_request:True and state:'merged')
```
