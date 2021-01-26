# \# PRs/MRs were open on X date.

This metric shows the number of open reviews in a given date.
- Today: number of issues that are open today.
- 1 month ago: number of issues that were open 1 month ago.
- 1 year ago: number of issues that were open 1 year ago.

## Elasticsearch query parameters
```
index: 'all'
filter: pull_request=True or merge_request=True
filter: 'terms', origin=urls
filter: created_at={'lte': date} and (closed_at={'gte': date} or merged_at={'gte': date} or state=['open', 'opened'])
```
