# Submitters onboarding / last active (PRs/MRs)

Number of review submitters onboarding vs review submitters last active in the period defined by the user.

```
index: 'all'
filter: pull_request:True or merge_request:True
range: from_date < 'grimoire_creation_date' < to_date
filter: 'terms', origin=urls
aggregation: 'terms', field:'author_uuid'
    metric: 'min', field:'grimoire_creation_date'
    metric: 'max', field:'grimoire_creation_date'
```
