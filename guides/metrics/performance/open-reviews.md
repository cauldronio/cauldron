# Open reviews

This metric shows the number of open reviews in a given date.

## Elasticsearch query parameters
```
index: 'all'
filter: pull_request=True or merge_request=True
filter: 'terms', origin=urls
filter: created_at={'lte': date} and (closed_at={'gte': date} or merged_at={'gte': date} or state=['open', 'opened'])
```
