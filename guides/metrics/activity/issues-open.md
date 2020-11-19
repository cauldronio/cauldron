# \# Issues open on X date.

Number of open issues on a date.
- Today: number of issues that are open today.
- 1 month ago: number of issues that were open 1 month ago.
- 1 year ago: number of issues that were open 1 year ago.

```
index: 'all'
filter: pull_request:False or is_gitlab_issue:1
filter: 'terms', origin=urls
must : range('created_at' < date) AND (range('closed_at' > date) OR match(state='open'))
```
