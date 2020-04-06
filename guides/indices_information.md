
## Indices 
An optimized collection of JSON documents. Each document is a collection of fields, the key-value pairs that contain your data. [1]

- [meetup_enriched_index](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/meetup.csv)
- [git_enrich_index](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/git.csv)
- [git_aoc_enriched_index](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/areas_of_code.csv)
- [gitlab_enriched_index](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/gitlab_issues.csv)
- [github_enrich_index](https://github.com/chaoss/grimoirelab-elk/blob/master/schema/github_issues.csv)

## Index aliases
The index aliases allows aliasing an index with a name. An alias can also be mapped to more than one index, and when specifying it, the alias will automatically expand to the aliased indices. [2]

### Related to GitHub
```
affiliations                        github_enrich_index
github_enrich                       github_enrich_index
github_issues                       github_enrich_index
github_issues_enrich                github_enrich_index
issues_closed                       github_enrich_index
issues_created                      github_enrich_index
issues_updated                      github_enrich_index
```

### Related to Git
```
git_aoc_enriched                    git_aoc_enriched_index
git_areas_of_code                   git_aoc_enriched_index
git                                 git_enrich_index
git_author                          git_enrich_index
git_enrich                          git_enrich_index
```

### Related to Gitlab
```
gitlab                              gitlab_enriched_index
gitlab_enriched                     gitlab_enriched_index
```

### Related to Meetup
```
meetup                              meetup_enriched_index
meetup_enriched                     meetup_enriched_index
```

### All data sources
```
ocean                               gitlab_enriched_index
                                    meetup_enriched_index
                                    git_enrich_index
                                    github_enrich_index
```
### Data sources with issue information
```
ocean_tickets                       gitlab_enriched_index
                                    github_enrich_index
                                    meetup_enriched_index
```


## Index patterns

To explore and visualize data in Kibana, you must create an index pattern. An index pattern tells Kibana which Elasticsearch indices contain the data that you want to work with. [3]

- github_enrich
- git_enrich
- git_aoc_enriched
- gitlab_enriched
- meetup_enriched
- ocean
- ocean_tickets

## References
[1] https://www.elastic.co/blog/what-is-an-elasticsearch-index

[2] https://www.elastic.co/guide/en/elasticsearch/reference/6.8/indices-aliases.html

[3] https://www.elastic.co/guide/en/kibana/current/index-patterns.html