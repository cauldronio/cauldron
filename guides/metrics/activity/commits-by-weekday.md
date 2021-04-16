# \# Commits by weekday

This bar chart shows how commit activity is distributed across the days of the week. When activity only occurs on workdays, the community may have mostly paid contributors who work during the week. Activity on the weekends may indicate volunteer activities. Exclude commits with the same hash across many repositories.

## Elasticsearch query parameters
```
index: 'git'
filter: 'files' is not 0
range: from_date < 'grimoire_creation_date' < to_date
filter: 'terms', origin=urls
aggregation: 'terms', script: "doc['grimoire_creation_date'].value.dayOfWeek"
aggregation: 'cardinality', field: 'hash'
```
