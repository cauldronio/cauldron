# Time open (average) - Issues

This metric shows the average time that open issues have been open.

```
index: 'all'
filter: pull_request=False or is_gitlab_issue=1
filter: 'terms', origin=urls
filter: created_at={'lte': date} and (closed_at={'gte': date} or state=['open', 'opened'])
```
