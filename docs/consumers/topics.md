# Consumer / Topics

Likeastore Topics API allows consumers to fetch relevant and trending content, grouped by particular topics.

## Topics

Few examples of topics,

* `web-development`
* `startups`
* `cloud-computing`
* `interface-design`
* `functional-programming`
* `marketing`
* `gaming`
* `travel`

and more.

Particular topic can be created based on set of keywords and other properties.

## Fetching Topics data

To fetch data by topics

```
HTTP GET /api/topics/:topicId
```

Example,

```
HTTP GET /api/topics/startups
```

## Seaching inside topic

You can search to particular term inside topic,

```
HTTP GET /api/topics/startups/search?text=techcrunch
```