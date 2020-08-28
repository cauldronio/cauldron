# Organizational diversity (Git)

Shows the number of git authors who contribute to a project grouped by their organization domain in the period defined by the user, ignoring pull/merge request commits.

* Top 10 domains
```
index: 'git'
range: from_date < 'grimoire_creation_date' < to_date
filter: 'files' is not 0
aggregation: 'terms', field:'author_domain', size:10, order:{'authors': 'desc'}
    metric: 'cardinality', field:'author_uuid'
```

* Rest of domains
```
index: 'git'
range: from_date < 'grimoire_creation_date' < to_date
filter: 'exists', field='author_domain'
filter: 'author_domain' must not 'match_phrase' domains_ignored
filter: 'files' is not 0
aggregation: 'cardinality', field:'author_uuid'
```
