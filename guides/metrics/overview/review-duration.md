# Review duration

Average time to merge a pull request or merge request in a period of time.

```
index: 'all'
average: 'time_to_close_days'
range: from_date < 'grimoire_creation_date' < to_date
filter: (pull_request:True and state:'closed') or (merge_request:True and state:'merged')
```
