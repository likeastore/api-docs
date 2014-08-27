# Consumers / Workflow

The description of typical integration workflow between Likeastore and API user (consumer).

## Data collection process

Except the few rare cases, all supported social media sources are using OAuth / OAuth 2.0 authorization to their API's. The result of OAuth authorization is `access_token` / `access_secret` which is used to access their data collection endpoints.

In order to collect that data, `access_token` / `access_secret` have to be submitted to server. Once `access_token` is retrieved, API user (consumer) schedules the data collection.

The data collection process, consist of 2 parts: **initial** collection and **continuous** collection. Initial collection is required to get all existing favorites of user (all current ones, available on time of request). Continuous collection will be collecting all new favorites and could notify API user that new data is available.

The API user receives **initial** data right after request, but also could use API to read and search the data after. The API user (consumer) is responsible for receiving `access_token` / `access_secret` on their own, in the same time we offer some helpful [intergration facilities](server.md).

All communication is done by HTTP, based on JSON payload. Future version of API will also provide WebSocket support for data streaming.

## Access tokens

To get the access token for user, client have to do following things:

1. Register their application (eg. [twitter](https://dev.twitter.com/), [github](https://github.com/settings/applications/new))
2. Implement OAuth web flow

To simplify OAuth web flow implementation, client might use platform based solutions (eg. [passport](http://passportjs.org/)) or use Likeastore [social networks authorization server](server.md).

## Rate limits

Many social networks implement `rate limiting` strategies, that might prevent featch the data after some rate overusage. Likeastore API and infrastructure take care of rate limiting, building optimal number of requests to fetch all data as fast as possible.

## Scheduling data collection

Once `access_token` is obtained, API user (consumer) needs to schedule data collection (with [social networks authorization server](server.md) it will done automatically).

It will be done by creating `connection` API object.

```plain
HTTP POST /api/connection
```

Payload,

```js
{
	user: 'user_id',
	accessToken: 'access_token',
	accessTokenSecret: 'access_token_secret',
	network: 'twitter'
}
```

The response, HTTP 201 (created).

It's possible to retrieve **initial** data collection results into connection reponse. Please note, that it would increase HTTP response time.

```plain
HTTP POST /api/connection?include_data=1
```

## Using REST hooks

After initial portion of data is collected, the **continuos** collection is completely async. To be notified of some action happend on Likeastore server, [REST hooks](http://resthooks.org/).

The the REST hooks would allow API user server to be triggered than different events occuring:

* Data is collected
* Access token is expired
* Errors

```plain
HTTP PUT /api/subscriptions
```

## Reading the data

The API user might access the data, by such endpoints.

```plain
HTTP GET /api/favorites/:user
HTTP GET /api/favorites/:user/:network
```

where `network` is type of enabled social network.

## Searching the data

It's also possible to search among user's data.

```plain
HTTP GET /api/search/:user?q=search+text
```