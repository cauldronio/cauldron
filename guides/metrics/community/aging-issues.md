# Submitters aging (Issues)

This chart shows how many new issue submitters joined the community during a corresponding period of time (attracted) and how many of these people are still active in the community (retained), that is, less than 3 months since their last contribution.

**NOTE**: The data shown corresponds to a snapshot of the end date of the period selected by the user.

More information: [Measure your open source communitie's age to keep it healthy](https://www.oreilly.com/content/measure-your-open-source-communitys-age-to-keep-it-healthy/)

```
index: 'all'
filter: pull_request:False or is_gitlab_issue:1
filter: 'terms', origin=urls
aggregation: 'terms', field:'author_uuid'
    metric: 'min', field:'grimoire_creation_date'
    metric: 'max', field:'grimoire_creation_date'
```
