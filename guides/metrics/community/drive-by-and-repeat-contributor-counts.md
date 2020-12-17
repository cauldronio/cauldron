# Drive-by and repeat contributor counts

This graph shows the number of new contributors in the specified time period and indicates how may were drive-by or repeat contributors. Drive-by contributors are contributors who make less than the required 5 contributions in the specified time period. Repeat contributors are contributors who made 5 or more contributions in the specified time period and their first contribution is in the specified time period.

## Elasticsearch query parameters
```
index: 'git'
range: 'grimoire_creation_date' < to_date
filter: 'terms', origin=urls
filter: 'files' is not 0
extra: size=0
aggregation: 'terms', field:'author_uuid'
     metric: 'min', field:'grimoire_creation_date'
     metric: 'cardinality', field:'hash'
```
