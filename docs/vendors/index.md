# Likeastore for Vendors

This API would allow 3rd party vendors (recomendation systems) to get the collection of their users favorites (likes) from different social medias into one sigle stream.

## Format

All data is returned in JSON format. Also all the data that is passed to the server, must be formatted as JSON message. To get JSONP-style responses, supply GET attribute <code>callback</code>. The <code>callback</code> parameter is the desired function name and must be alphanumeric.

## Supported media providers

* [Twitter]()
* [Github]()
* [Stackoverflow]()
* [Facebook]()
* [Vimeo]()
* [Youtube]()
* [Dribbble]()
* [Behance]()
* [Pocket]()
* [Tumblr]()
* [Instagram]()
* [Flickr]()

Planned to be added soon:

* [Last.fm]()
* [Soundcloud]()
* [Pinterest]()

## Endpoints

* [Authorization](/api-docs/vendor/authorization)
* [Schedule data collection](/api-docs/vendor/collection)
* [Web hooks](/api-docs/vendor/webhooks)
* [Retreiving favorites](/api-docs/vendor/retreive)
* [Search](/api-docs/vendor/search)

## Integration helpers

* [Connect network widget](/api-docs/vendor/widget)
* [Social networks authorization server](/api-docs/vendor/server)

## Use cases

* [Likeastore integration use case](/api-docs/vendor/usecase)

All questions please forward to [devs@likeastore.com](mailto:devs@likeastore.com).