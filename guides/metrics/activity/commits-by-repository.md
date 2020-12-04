# \# Commits by repository

Shows the number of git commits of a project grouped by repository in the period defined by the user, ignoring empty commits.

* Top 10 repositories
```
index: 'git'
range: from_date < 'grimoire_creation_date' < to_date
filter: 'files' is not 0
aggregation: 'terms', field:'repo_name', size:10, order:{'commits': 'desc'}
    metric: 'cardinality', field:'hash'
```

* Rest of repositories
```
index: 'git'
range: from_date < 'grimoire_creation_date' < to_date
filter: 'exists', field='repo_name'
filter: 'repo_name' must not 'match_phrase' repos_ignored
filter: 'files' is not 0
aggregation: 'cardinality', field:'hash'
```
