# Submitters retained ratio (PRs/MRs)

This chart shows the ratio between retained (less than 3 months since user's last contribution) and non-retained review submitters in a community.

**NOTE**: The data displayed corresponds to the time of last data refresh.

```
index: 'all'
filter: pull_request:True or merge_request:True
aggregation: 'terms', field:'author_uuid'
    metric: 'min', field:'grimoire_creation_date'
    metric: 'max', field:'grimoire_creation_date'
```
