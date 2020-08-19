# \# Commits by hour of day

Number of commits by day time in the period defined by the user, ignoring pull/merge request commits.

```
index: 'git'
filter: 'files' is not 0
range: from_date < 'grimoire_creation_date' < to_date
aggregation: 'terms', script: "doc['grimoire_creation_date'].value.getHourOfDay()"
```
