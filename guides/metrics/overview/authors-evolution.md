# \# Authors

Number of authors gives an idea of the size of the active community for a project. In this case, we're measuring, for each week in the chart, the number of different identities that authored at least one commit, or that submitted issues or reviews (pull or merge requests) to any repository of the project during that week. Although this is usually a good indicator of people who are active in the project, it is important to notice that, during any given week, active developers may be busy with some other stuff, thus not appearing in this chart. Also, casual contributors (such as somebody submitting a bug report but not really engaged with the project) appear in the chart. People taking care of important tasks, such as writing documentation, may also be reflected in this chart, or not, depending on the repositories included in the project, and how the project deals with those tasks.

If the project description includes Meetup groups, people rsvp'ing meetings in those groups are also shown in the chart (Attendees)

**Important details**:  We say "identities" and not "persons" because, a certain person could commit, or submit an issue or a review, with different identities. This happens mainly because people change their identities (name, email address), or because they use different identitis (for example, names with slight differences, or corporate or personal email addresses or GitHub handles), and is uncommon during a single week (thus the numbers in the chart tend to be accurate in most cases).

## Elasticsearch query parameters
```
index: 'all'
unique count: 'author_uuid'
range: from_date < 'grimoire_creation_date' < to_date
filter: 'terms', origin=urls
aggregation: 'date_histogram', field: 'grimoire_creation_date', calendar_interval: '1w'
filters: {
  'Authors': is_git_commit:1,
  'Submitters (issues)': pull_request:False or is_gitlab_issue:1,
  'Submitters (reviews)': pull_request:True or merge_request:True,
  'Observers': is_meetup_rsvp:1
}
```
