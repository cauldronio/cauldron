# \# Commits by hour of day

Number of commits by day time in the period defined by the user, ignoring pull/merge request commits. Exclude commits with the same hash across many repositories.

```
index: 'git'
filter: 'files' is not 0
range: from_date < 'grimoire_creation_date' < to_date
filter: 'terms', origin=urls
aggregation: 'terms', script: "doc['grimoire_creation_date'].value.getHourOfDay()"
aggregation: 'cardinality', field: 'hash'
```
