## Index patterns for Kibana

To explore and visualize data in Kibana, you must create an index pattern. An index pattern tells Kibana which Elasticsearch indices contain the data that you want to work with. [1]

- [**git**](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/git.csv): Git commits and authors
- [**github**](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/github_issues.csv): GitHub issues and pull requests.
- [**github_comments**](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/github2_issues.csv): GitHub commentaries in issues and pull requests
- [**github_repo**](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/github_repos.csv): GitHub information related about the repositories
- [**gitlab_issues**](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/gitlab_issues.csv): GitLab issues
- [**gitlab_mrs**](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/gitlab_merges.csv): GitLab merge requests
- [**meetup**](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/meetup.csv): Meetup events
- **all**: All the index patterns in one
- **all_tickets**: Indices related with tickets (GitHub issues and Gitlab issues together)

 *Deprecated index-patterns. Could be removed in a future release with a notification in Cauldron*

- [**git_enrich**](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/git.csv): Git commits and authors
- [**github_enrich**](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/github_issues.csv): GitHub issues and pull requests.
- [**github2**](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/github2_issues.csv): GitHub commentaries in issues and pull requests
- [**github_repo_enrich**](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/github_repos.csv): GitHub information related about the repositories
- [**gitlab_enriched**](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/gitlab_issues.csv): GitLab issues
- [**gitlab_merge_requests**](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/gitlab_merges.csv): GitLab merge requests
- [**meetup_enriched**](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/meetup.csv): Meetup events
- **ocean**: All the index patterns in one
- **ocean_tickets**: Indices related with tickets (GitHub issues and Gitlab issues together)

## Indices 
Indices are an optimized collection of JSON documents. Each document is a collection of fields, the key-value pairs that contain your data. [2]

- [meetup_enriched_index](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/meetup.csv)
- [git_enrich_index](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/git.csv)
- [gitlab_enriched_index](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/gitlab_issues.csv)
- [gitlab_mrs_enriched_index](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/gitlab_merges.csv)
- [github_enrich_index](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/github_issues.csv)
- [github_repo_enrich_index](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/github_repos.csv)
- [github2_enrich_index](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/github2_issues.csv)

## Index aliases
Index aliases allows aliasing an index with a name. An alias can also be mapped to more than one index, and when specifying it, the alias will automatically expand to the aliased indices. [3]

### Related to GitHub
```
Alias                               Index
=====                               =====
github                              github_enrich_index
github_repo                         github_repo_enrich_index
github_comments                     github2_enrich_index
```

### Related to Git
```
Alias                               Index
=====                               =====
git                                 git_enrich_index
```

### Related to Gitlab
```
Alias                               Index
=====                               =====
gitlab_issues                       gitlab_enriched_index
gitlab_mrs                          gitlab_mrs_enriched_index
```

### Related to Meetup
```
Alias                               Index
=====                               =====
meetup                              meetup_enriched_index
```

### All data sources
```
Alias                               Index
=====                               =====
all                                 gitlab_enriched_index
                                    meetup_enriched_index
                                    git_enrich_index
                                    github_enrich_index
                                    gitlab_mrs_enriched_index
```
### Data sources with issue information
```
Alias                               Index
=====                               =====
all_tickets                         gitlab_enriched_index
                                    github_enrich_index
```

## References

[1] https://www.elastic.co/guide/en/kibana/current/index-patterns.html

[2] https://www.elastic.co/blog/what-is-an-elasticsearch-index

[3] https://www.elastic.co/guide/en/elasticsearch/reference/6.8/indices-aliases.html

