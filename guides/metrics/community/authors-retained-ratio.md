# Authors retained ratio (Git)

This chart shows the ratio between retained (less than 3 months since user's last contribution) and non-retained people in a community.

**NOTE**: The data displayed corresponds to the time of last data crunching.

```
index: 'git'
filter: 'files' is not 0
aggregation: 'terms', field:'author_uuid'
    metric: 'min', field:'grimoire_creation_date'
    metric: 'max', field:'grimoire_creation_date'
```
