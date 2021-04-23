# \# People answering (Chart)

Number of people answering questions on StackExchange in a period, grouped by date.

## Elasticsearch query parameters
```
index: 'stackexchange'
range: from_date < 'grimoire_creation_date' < to_date
filter: 'match', is_stackexchange_answer='1'
filter: 'terms', tag=urls
aggregation: 'date_histogram', field='grimoire_creation_date'
aggregation: 'cardinality', field='author'
```
