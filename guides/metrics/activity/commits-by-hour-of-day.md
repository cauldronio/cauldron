# \# Commits by hour of day

Number of commits by day time in all the time, ignoring pull/merge request commits.

```
index: 'git'
filter: 'files' is not 0
aggregation: 'terms', script: "doc['grimoire_creation_date'].value.getHourOfDay()"
```
