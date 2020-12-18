# \# Reviews started/closed

Number of reviews shows activity related to pull requests (GitHub) or merge requests (GitLab). This chart shows, for each week, the number of merge or pull requests that were submitted (started), and decided (closed). Pull and merge reviews are the mechanism used for reviewing code changes that are proposed to enter repositories. Closing a pull or merge request can be done by accepting the change, or by declining it. As with issues, a larger number of started reviews than closed reviews means that the project is not coping with all proposals for code change that are being submitted.

**Important details**: Even when it is considered a good practice, not all projects are using it, or not for all changes. Also, the code changes in a merge or pull request may include one or more commits, depending on the policies of the project.

## Elasticsearch query parameters
```
index: 'all'
filter: pull_request:True or merge_request:True
filter: 'terms', origin=urls
extra: size=0
<open>
    aggregation: 'filter': range(from_date < created_at < to_date)
    aggregation: 'date_histogram', field: 'created_at', calendar_interval: '1w'
<closed>
    aggregation: 'filter': range(from_date < closed_at < to_date)
    aggregation: 'date_histogram', field: 'closed_at', calendar_interval: '1w'
<merged>
    aggregation: 'filter': range(from_date < merged_at < to_date)
    aggregation: 'date_histogram', field: 'merged_at', calendar_interval: '1w'
```
