# Mean and median duration (days) of all closed reviews

This heat map compares the responsiveness of a repository to reviews (pull requests and merge requests). The light blue indicates review response times that are fastest; the red indicates the time slots with slowest response times. White boxes indicate time slots in which no reviews were closed. The minimum and maximum are determined by the pool of repositories within the project. For GitHub repositories, both accepted and declined pull requests are taking into account. For GitLab repositories, only the declined are being shown.

## Elasticsearch query parameters
```
index: 'all'
filter: pull_request=True or merge_request=True
filter: 'terms', origin=urls
filter: closed_at={'gte': from_date, "lte": to_date}
extra: size=0
aggregation: 'date_histogram', field='closed_at', format='yyyy-MM-dd'
     metric: 'avg', field='time_to_close_days'
     metric: 'percentiles', field='time_to_close_days', percents=[50]
```
