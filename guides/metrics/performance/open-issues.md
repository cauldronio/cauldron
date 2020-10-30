# Open issues

This metric shows the number of open issues in a given date.

```
index: 'all'
filter: pull_request=False or is_gitlab_issue=1
filter: created_at={'lte': date} and (closed_at={'gte': date} or state=['open', 'opened'])
```
