# Community aging

This chart shows how many new people joined the community during a corresponding period of time (attracted) and how many of these people are still active in the community (retained), that is, less than 3 months since their last contribution.

**NOTE**: The data displayed corresponds to the time of last data crunching.

```
index: 'all'
aggregation: 'terms', field:'author_uuid'
    metric: 'min', field:'grimoire_creation_date'
    metric: 'max', field:'grimoire_creation_date'
```
