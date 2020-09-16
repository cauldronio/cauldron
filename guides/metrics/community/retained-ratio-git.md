# Authors retained ratio (Git)

This chart shows the ratio between retained (less than 3 months since user's last contribution) and non-retained git authors in a community.

**NOTE**: The data shown corresponds to a snapshot of the end date of the period selected by the user.

```
index: 'git'
filter: 'files' is not 0
aggregation: 'terms', field:'author_uuid'
    metric: 'min', field:'grimoire_creation_date'
    metric: 'max', field:'grimoire_creation_date'
```
