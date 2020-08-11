# \# Commits by weekday

Number of commits by weekday in all the time, ignoring merge request commits (at least 1 file changed).

```
index: 'git'
filter: 'files' is not 0
aggregation: 'terms', script: "doc['grimoire_creation_date'].value.dayOfWeek"
```
