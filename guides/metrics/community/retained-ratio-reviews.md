# Submitters retained ratio (PRs/MRs)

This chart shows the ratio between retained (less than 3 months since user's last contribution) and non-retained review submitters in a community.

**NOTE**: The data shown corresponds to a snapshot of the end date of the period selected by the user.

```
index: 'all'
filter: pull_request:True or merge_request:True
filter: 'terms', origin=urls
aggregation: 'terms', field:'author_uuid'
    metric: 'min', field:'grimoire_creation_date'
    metric: 'max', field:'grimoire_creation_date'
```
