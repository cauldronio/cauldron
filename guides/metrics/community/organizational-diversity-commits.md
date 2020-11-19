# Organizational diversity (Git) - Commits

Shows the number of git commits of a project grouped by the organization domain of their authors in the period defined by the user, ignoring pull/merge request commits.

* Top 10 domains
```
index: 'git'
range: from_date < 'grimoire_creation_date' < to_date
filter: 'files' is not 0
filter: 'terms', origin=urls
aggregation: 'terms', field:'author_domain', size:10, order:{'commits': 'desc'}
    metric: 'cardinality', field:'hash'
```

* Rest of domains
```
index: 'git'
range: from_date < 'grimoire_creation_date' < to_date
filter: 'exists', field='author_domain'
filter: 'author_domain' must not 'match_phrase' domains_ignored
filter: 'files' is not 0
filter: 'terms', origin=urls
aggregation: 'cardinality', field:'hash'
```
