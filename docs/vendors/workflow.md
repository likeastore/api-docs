# Vendors API / Workflow

The description of typical integration workflow between Likeastore and API user (consumer).

## Data collection process

Except the few rare cases, all supported social media sources are using OAuth / OAuth 2.0 authorization to their API's. The result of OAuth authorization is `access_token` / `access_secret` which is used to access their data collection endpoints.

In order to collect that data, `access_token` / `access_secret` have to be submitted to server. Once `access_token` is retrieved, API user (consumer) schedules the data collection.

The data collection process, consist of 2 parts: **initial** collection and **continuous** collection. Initial collection is required to get all existing favorites of user (all current ones, available on time of request). Continuous collection will be collecting all new favorites and could notify API user that new data is available.

The API user receives **initial** data right after request, but also could use API to read and search the data after. The API user (consumer) is responsible for receiving `access_token` / `access_secret` on their own, in the same time we offer some helpful [intergration facilities]().

All communication is done by HTTP, based on JSON payload. Future version of API will also provide WebSocket support for data streaming.

## Access tokens

## Rate limits

## Retrieving Access tokens

## Scheduling data collection

## Using Web hooks

## Reading the data

## Searching the data

