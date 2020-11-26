# \# Commits (chart)

Number of commits is the most common measure of activity in a git repository. To compute it, we're considering all commits in all branches of all repositories in the project, excluding empty commits. Each commit represents a change to the source code, maybe touching several files. However, commits may be very different in size, complexity and usefulness to the project, so this number should only be considered as an indicator, among others.

**Important details**: Because of the way people work with git repositories, it is usual that the latest commits that developers are producing are still in their personal repositories, maybe following a review process, and were still not merged in the repositories that we track. Because of that, it is usual that for the last few days (or in some cases, weeks), there is a severe underestimation of the number of commits. As time passes, it is usual that the count of commits for that period increases, as all those "pending" commits find their way to the repository.

## Elasticsearch query parameters
```
index: 'git'
filter: 'files' is not 0
range: from_date < 'grimoire_creation_date' < to_date
filter: 'terms', origin=urls
aggregation: 'date_histogram', field: 'grimoire_creation_date', calendar_interval: '1w'
```
