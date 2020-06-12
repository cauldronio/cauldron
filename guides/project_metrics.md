# Project metrics

## Commits Activity

### \#Commits
Number of commits, ignoring pull/merge request commits.
- Last month: from 1 month ago to now.
- Last year: from 1 year ago to now.
- Year-over-year: comparison of commits from last year to the previous year.

```
index: 'git'
unique count: 'hash'
range: from_date < 'grimoire_creation_date' < to_date
filter: 'files' is not 0
``` 

### \#Lines/commit
Average lines changed per commit, ignoring pull/merge request commits.
- Last month: from 1 month ago to now.
- Last year: from 1 year ago to now.
- Year-over-year: comparison of lines/commit from last year to the previous year.
```
index: 'git'
average: 'lines_changed'
range: from_date < 'grimoire_creation_date' < to_date
filter: 'files' is not 0
```

### \#Files
Number of files changed
- Last month: from 1 month ago to now.
- Last year: from 1 year ago to now.
```
index: 'git'
sum: 'files'
range: from_date < 'grimoire_creation_date' < to_date
```

### \#Lines/commit/file
Average of lines changed per file and commit, ignoring pull/merge request commits.
- Last month: from 1 month ago to now.
- Last year: from 1 year ago to now.
- Year-over-year: comparison of lines/file/commit from last year to the previous year.

```
'#Lines/commit' / '#Files'
```


### \# Commits over time
Evolution of the number of commits in the period defined by the user, ignoring pull/merge request commits.
```
index: 'git'
filter: 'files' is not 0
range: from_date < 'grimoire_creation_date' < to_date
aggregation: 'date_histogram', field: 'grimoire_creation_date', calendar_interval: '1w'
```

### \# Lines added vs removed
Number of lines added vs removed in the period defined by the user.
```
index: 'git'
range: from_date < 'grimoire_creation_date' < to_date
aggregation: 'date_histogram', field: 'grimoire_creation_date', calendar_interval: '1w'
aggregation: 'sum', script: "doc['lines_removed'].value * -1"
aggregation: 'sum', field: 'lines_added'
```

### \# Commits by hour of day
Number of commits by day time in all the time, ignoring pull/merge request commits.
```
index: 'git'
filter: 'files' is not 0
aggregation: 'terms', script: "doc['grimoire_creation_date'].value.getHourOfDay()"
```

### \# Commits by weekday
Number of commits by weekday in all the time, ignoring merge request commits (at least 1 file changed).
```
index: 'git'
filter: 'files' is not 0
aggregation: 'terms', script: "doc['grimoire_creation_date'].value.dayOfWeek"
```


## Issues Activity

### \# Issues opened
Number of created issues in a period of time
- Last month: from 1 month ago to now.
- Last year: from 1 year ago to now.
- Year-over-year: comparison of issues created from last year to the previous year.
```
index: 'all'
range: from_date < 'created_at' < to_date
filter: pull_request:False or is_gitlab_issue:1
```

### \# Issues closed
Number of closed issues in a period of time
- Last month: from 1 month ago to now.
- Last year: from 1 year ago to now.
- Year-over-year: comparison of issues closed from last year to the previous year.
```
index: 'all'
range: from_date < 'closed_at' < to_date
filter: pull_request:False or is_gitlab_issue:1
filter: 'state' is 'closed'
```

### \# Issues open on X date.
Number of open issues on a date.
- Today: number of issues that are open today.
- 1 month ago: number of issues that were open 1 month ago.
- 1 year ago: number of issues that were open 1 year ago.
```
index: 'all'
filter: pull_request:False or is_gitlab_issue:1
must : range('created_at' < date) AND (range('closed_at' > date) OR match(state='open'))
```


### \# Issues open/closed
Open and closed issues by date in the period defined by the user.
```
index: 'all'
filter: pull_request:False or is_gitlab_issue:1
<open>
    aggregation: 'filter': range(from_date < created_at < to_date)
    aggregation: 'date_histogram', field: 'created_at', calendar_interval: '1w'
<closed>
    aggregation: 'filter': range(from_date < closed_at < to_date)
    aggregation: 'date_histogram', field: 'closed_at', calendar_interval: '1w'
```

### \# Open issues age
Since when they are created the issues that are currently open.
```
index: 'all'
filter: (pull_request:False or is_gitlab_issue:1) and state:'open'
aggregation: 'date_histogram', field: 'created_at', calendar_interval: '1w'
```

### \# Issues open by weekday
Get when the issues are opened by weekday.
```
index: 'git'
filter: (pull_request:False or is_gitlab_issue:1)
aggregation: 'terms', script: "doc['created_at'].value.dayOfWeek"
```

### \# Issues closed by weekday
Get when the issues are closed by weekday.
```
index: 'git'
filter: (pull_request:False or is_gitlab_issue:1)
aggregation: 'terms', script: "doc['closed_at'].value.dayOfWeek"
```


## Pull Requests and Merge Requests Activity

### \# PRs/MRs opened
Number of new Pull/Merge Requests in a period of time
- Last month: from 1 month ago to now.
- Last year: from 1 year ago to now.
- Year-over-year: comparison of PRs/MRs created from last year to the previous year.
```
index: 'all'
range: from_date < 'created_at' < to_date
filter: pull_request:True or merge_request:True
```

### \# PRs/MRs closed
Number of closed Pull/Merge Requests in a period of time
- Last month: from 1 month ago to now.
- Last year: from 1 year ago to now.
- Year-over-year: comparison of PRs/MRs closed from last year to the previous year.
```
index: 'all'
range: from_date < 'closed_at' < to_date
filter: pull_request:True or merge_request:True
```

### \# PRs/MRs were open on X date.
Number of open issues on a date.
- Today: number of issues that are open today.
- 1 month ago: number of issues that were open 1 month ago.
- 1 year ago: number of issues that were open 1 year ago.
```
index: 'all'
filter: pull_request:True or merge_request:True
must : range('created_at' < date) AND (range('closed_at' > date) OR match(state='open'))
```


### \# Reviews open/closed
Open and closed PRs/MRs by date in the period defined by the user.
```
index: 'all'
filter: pull_request:True or merge_request:True
<open>
    aggregation: 'filter': range(from_date < created_at < to_date)
    aggregation: 'date_histogram', field: 'created_at', calendar_interval: '1w'
<closed>
    aggregation: 'filter': range(from_date < closed_at < to_date)
    aggregation: 'date_histogram', field: 'closed_at', calendar_interval: '1w'
```

### \# Open reviews age
Since when they are created the PRs/MRs that are currently open.
```
index: 'all'
filter: (pull_request:True or merge_request:True) and state:'open'
aggregation: 'date_histogram', field: 'created_at', calendar_interval: '1w'
```

### \# Reviews open by weekday
Get when the PRs/MRs are opened by weekday.
```
index: 'git'
filter: pull_request:True or merge_request:True
aggregation: 'terms', script: "doc['created_at'].value.dayOfWeek"
```

### \# Reviews closed by weekday
Get when the PRs/MRs are closed by weekday.
```
index: 'git'
filter: pull_request:True or merge_request:True
aggregation: 'terms', script: "doc['closed_at'].value.dayOfWeek"
```
