# \# Commits by weekday

Number of commits by weekday in the period defined by the user, ignoring merge request commits (at least 1 file changed).

```
index: 'git'
filter: 'files' is not 0
range: from_date < 'grimoire_creation_date' < to_date
filter: 'terms', origin=urls
aggregation: 'terms', script: "doc['grimoire_creation_date'].value.dayOfWeek"
```
