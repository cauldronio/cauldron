# Submitters onboarding / last active (Issues)

Number of issue submitters onboarding vs issue submitters last active in the period defined by the user.

```
index: 'all'
filter: pull_request:False or is_gitlab_issue:1
range: from_date < 'grimoire_creation_date' < to_date
filter: 'terms', origin=urls
aggregation: 'terms', field:'author_uuid'
    metric: 'min', field:'grimoire_creation_date'
    metric: 'max', field:'grimoire_creation_date'
```
