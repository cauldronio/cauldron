# \# Issues created

Number of created issues in a period of time.

## Elasticsearch query parameters
```
index: 'all'
range: from_date < 'created_at' < to_date
filter: 'terms', origin=urls
filter: pull_request:False or is_gitlab_issue:1
```
