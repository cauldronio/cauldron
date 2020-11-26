# \# Issues created/closed

Number of issues shows activity in the issue tracking system, usually including bug reports, feature requests, and other tasks that are tracked with issues (tickets). We measure, for each week, the number of issues that were opened (created) or closed during it. Not only the absolute numbers, but also the relationship between open and closed issues is important in this chart: if many more issues are consistently being opened than closed, the project is not dealing with all the new stuff that is entering the issue tracking system.

**Important details**: Some projects using git repositories in GitHub or GitLab are dealing with issues elsewhere (for example, their own instance of Bugzilla or Jira). So, in some cases this chart can be flat, or show a really low activity, just because that activity is happening somewhere else. Also, different projects may use issues in different ways, from only tracking bugs reported by users, to dealing with all the bug fixing, feature implementation, and other tasks performed by the project.

## Elasticsearch query parameters
```
index: 'all'
filter: pull_request:False or is_gitlab_issue:1
filter: 'terms', origin=urls
<open>
    aggregation: 'filter': range(from_date < created_at < to_date)
    aggregation: 'date_histogram', field: 'created_at', calendar_interval: '1w'
<closed>
    aggregation: 'filter': range(from_date < closed_at < to_date)
    aggregation: 'date_histogram', field: 'closed_at', calendar_interval: '1w'
```
