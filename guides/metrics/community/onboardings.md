# \# Onboardings

Number of git authors, issue authors and review submitters entering in a project for a period of time.

* Git authors
```
index: 'git'
range: from_date < 'grimoire_creation_date' < to_date
filter: 'files' is not 0
filter: 'terms', origin=urls
aggregation: 'terms', field:'author_uuid'
    metric: 'min', field:'grimoire_creation_date'
```

* Issue authors
```
index: 'all'
range: from_date < 'grimoire_creation_date' < to_date
filter: pull_request:False or is_gitlab_issue:1
filter: 'terms', origin=urls
aggregation: 'terms', field:'author_uuid'
    metric: 'min', field:'grimoire_creation_date'
```

* PRs/MRs submitters
```
index: 'all'
range: from_date < 'grimoire_creation_date' < to_date
filter: pull_request:True or merge_request:True
filter: 'terms', origin=urls
aggregation: 'terms', field:'author_uuid'
    metric: 'min', field:'grimoire_creation_date'
```
