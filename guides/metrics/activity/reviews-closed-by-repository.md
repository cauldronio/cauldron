# \# Reviews closed by repository

Shows the number of reviews closed in a project grouped by repository in the period defined by the user.

* Top 10 repositories
```
index: 'all'
range: (from_date < 'closed_at' < to_date) OR (from_date < 'merged_at' < to_date)
filter: pull_request:True or merge_request:True
aggregation: 'terms', field:'repository', size:10
```

* Rest of repositories
```
index: 'all'
range: (from_date < 'closed_at' < to_date) OR (from_date < 'merged_at' < to_date)
filter: 'exists', field='repository'
filter: 'repository' must not 'match_phrase' repos_ignored
filter: pull_request:True or merge_request:True
```
