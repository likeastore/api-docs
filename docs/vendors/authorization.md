# Likeastore for Vendors - Authorization

Likeastore vendors API requires authentication for all endpoints. At the moment we support token based authorization.

## Register the application

In order to retrieve `client_id` and `client_secret`, please email to [devs@likeastore.com](mailto:devs@likeastore.com). You application will be registered and details will be sent back to you.

## Retrieve access token

```plain
HTTP POST /api/auth
```

### Parameters

| Name | Type | Description |
|---|---|---|
| **client_id**  | string  | **Required** The ID you received during application registration |
| **client_secret**  | string  | **Required** The Secret you received during application registration |

### Response

If `client_id` and `client_secret` is valid, the access_token returned as payload.

```js
{
	access_token: "4cc9cbeeecc44aac7c91708ac6c5e064632301a5"
}
```

## Access token usage

The valid access token should be submitted to server with each HTTP call by any of following options.

### HTTP headers

`X-Likeastore-Access-Token` header parameter.

### Query string

`?access_token=` query parameter.

### Cookie value

`lkstr_access_token` cookie value.

