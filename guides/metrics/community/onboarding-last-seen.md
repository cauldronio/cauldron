# \# Onboarding vs Last seen

Number of people entering vs last seen people in the period defined by the user.

```
index: 'all'
range: from_date < 'grimoire_creation_date' < to_date
aggregation: 'terms', field:'author_uuid'
    metric: 'min', field:'grimoire_creation_date'
    metric: 'max', field:'grimoire_creation_date'
```
