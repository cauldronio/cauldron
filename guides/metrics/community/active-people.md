# \# Active people

Number of git authors, issue authors and review submitters for a project for a period of time.

* Git authors
```
index: 'git'
unique count: 'author_uuid'
range: from_date < 'grimoire_creation_date' < to_date
filter: 'files' is not 0
```

* Issue authors
```
index: 'all'
unique count: 'author_uuid'
range: from_date < 'grimoire_creation_date' < to_date
filter: pull_request:False or is_gitlab_issue:1
```

* PRs/MRs submitters
```
index: 'all'
unique count: 'author_uuid'
range: from_date < 'grimoire_creation_date' < to_date
filter: pull_request:True or merge_request:True
```
