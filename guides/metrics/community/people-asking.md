# \# People asking

Number of people asking questions on StackExchange in a period.

## Elasticsearch query parameters
```
index: 'stackexchange'
range: from_date < 'grimoire_creation_date' < to_date
filter: 'match', is_stackexchange_question='1'
filter: 'terms', tag=urls
aggregation: 'cardinality', field='author'
```
