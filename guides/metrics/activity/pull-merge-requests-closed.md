# \# PRs/MRs closed

Number of closed (merged included) Pull/Merge Requests in a period of time
- Last month: from 1 month ago to now.
- Last year: from 1 year ago to now.
- Year-over-year: comparison of PRs/MRs closed from last year to the previous year.

## Elasticsearch query parameters
```
index: 'all'
range: (from_date < 'closed_at' < to_date) | (from_date < 'merged_at' < to_date)
filter: 'terms', origin=urls
filter: pull_request:True or merge_request:True
```
