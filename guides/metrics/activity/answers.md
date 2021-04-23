# \# Answers

Number of StackExchange answers in a period.

## Elasticsearch query parameters
```
index: 'stackexchange'
range: from_date < 'grimoire_creation_date' < to_date
filter: 'match', is_stackexchange_answer='1'
filter: 'terms', tag=urls
aggregation: 'cardinality', field='answer_id'
```
