# Time open (median) - Reviews

This metric shows the median time that open reviews have been open.

```
index: 'all'
filter: pull_request=True or merge_request=True
filter: created_at={'lte': date} and (closed_at={'gte': date} or state=['open', 'opened'])
```
