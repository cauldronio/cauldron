# Issues Closed Heatmap

Number of issues closed by weekday and by day time in the period defined by the user.

```
index: 'all'
filter: pull_request:False or is_gitlab_issue:1
range: from_date < 'closed_at' < to_date
aggregation: 'terms', script: "doc['closed_at'].value.dayOfWeek", size:7, order={'_term': 'asc'}
aggregation: 'terms', script: "doc['closed_at'].value.getHourOfDay()", size:24, order={'_term': 'asc'}
```
