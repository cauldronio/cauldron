# \# Authors per category over time

Evolution of the number of authors (contributors, maintainers, observers, and users) in the period defined by the user.

```
index: 'all'
unique count: 'author_uuid'
range: from_date < 'grimoire_creation_date' < to_date
aggregation: 'date_histogram', field: 'grimoire_creation_date', calendar_interval: '1w'
filters: {
  'Maintainers': is_git_commit:1,
  'Contributors': pull_request:True or merge_request:True,
  'Users': pull_request:False or is_gitlab_issue:1,
  'Observers': is_meetup_rsvp:1
}
```
