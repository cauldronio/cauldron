# \# Authors

Number of authors gives an idea of the size of the active developer community for a project. In this case, we're measuring, for each week in the chart, the number of different identities that authored at least one commit in git repositories of the project during that week. Although this is usually a good indicator of developers who are active in the project, it is important to notice that, during any given week, active developers may be busy with some complex code change that will produce no commit during the week, or reviewing code, or in any other task related to the project, but not appearing in this chart. People taking care of other important tasks, such as writing documentation, may also be reflected in this chart, or not, depending on the repositories included in the project, and on the fact that those tasks are reflected in commits, or not.

**Important details**:  We say "identities" and not "persons" because, a certain developer could commit with different identities. This happens mainly because developers update their identities (name, email address), or because they use different accounts with slight differences (eg, including or not a middle name, or using their corporate or personal email addresses), and is uncommon during the same week.

## Elasticsearch query parameters
```
index: 'all'
unique count: 'author_uuid'
range: from_date < 'grimoire_creation_date' < to_date
filter: 'terms', origin=urls
aggregation: 'date_histogram', field: 'grimoire_creation_date', calendar_interval: '1w'
filters: {
  'Maintainers': is_git_commit:1,
  'Contributors': pull_request:True or merge_request:True,
  'Users': pull_request:False or is_gitlab_issue:1,
  'Observers': is_meetup_rsvp:1
}
```
