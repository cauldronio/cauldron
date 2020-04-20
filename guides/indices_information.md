
## Indices 
Indices are an optimized collection of JSON documents. Each document is a collection of fields, the key-value pairs that contain your data. [1]

- [meetup_enriched_index](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/meetup.csv)
- [git_enrich_index](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/git.csv)
- [gitlab_enriched_index](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/gitlab_issues.csv)
- [gitlab_mrs_enriched_index](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/gitlab_merges.csv)
- [github_enrich_index](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/github_issues.csv)
- [github_repo_enrich_index](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/github_repos.csv)
- [github2_enrich_index](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/github2_issues.csv)

## Index aliases
Index aliases allows aliasing an index with a name. An alias can also be mapped to more than one index, and when specifying it, the alias will automatically expand to the aliased indices. [2]

### Related to GitHub
```
Alias                               Index
=====                               =====
affiliations                        github_enrich_index
github_enrich                       github_enrich_index
github_issues                       github_enrich_index
github_issues_enrich                github_enrich_index
issues_closed                       github_enrich_index
issues_created                      github_enrich_index
issues_updated                      github_enrich_index
github2                             github2_enrich_index
github_repo_enrich                  github_repo_enrich
github                              github_repo_enrich
```

### Related to Git
```
Alias                               Index
=====                               =====
git                                 git_enrich_index
git_author                          git_enrich_index
git_enrich                          git_enrich_index
```

### Related to Gitlab
```
Alias                               Index
=====                               =====
gitlab                              gitlab_enriched_index
gitlab_enriched                     gitlab_enriched_index
gitlab_merge_requests               gitlab_mrs_enriched_index
gitlab_mrs_enriched                 gitlab_mrs_enriched_index
```

### Related to Meetup
```
Alias                               Index
=====                               =====
meetup                              meetup_enriched_index
meetup_enriched                     meetup_enriched_index
```

### All data sources
```
Alias                               Index
=====                               =====
ocean                               gitlab_enriched_index
                                    meetup_enriched_index
                                    git_enrich_index
                                    github_enrich_index
                                    gitlab_mrs_enriched_index
```
### Data sources with issue information
```
Alias                               Index
=====                               =====
ocean_tickets                       gitlab_enriched_index
                                    github_enrich_index
```


## Index patterns

To explore and visualize data in Kibana, you must create an index pattern. An index pattern tells Kibana which Elasticsearch indices contain the data that you want to work with. [3]

- **github_enrich**: Issues and Pull requests.
- **github2**: Commentaries in Issues and Pull requests
- **github_repo_enrich**: Information related about the repositories
- **git_enrich**: Commits and authors
- **gitlab_enriched**: Issues
- **gitlab_merge_requests**: Merge requests
- **meetup_enriched**: Events
- **ocean**: All the index patterns in one
- **ocean_tickets**: Indices related with tickets. GitHub Issues and Gitlab Issues

## References
[1] https://www.elastic.co/blog/what-is-an-elasticsearch-index

[2] https://www.elastic.co/guide/en/elasticsearch/reference/6.8/indices-aliases.html

[3] https://www.elastic.co/guide/en/kibana/current/index-patterns.html