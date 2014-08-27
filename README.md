# Likeastore API

The Likeastore API documentation

## Overview

Likeastore open API allows users and consumers to integrate and fetch and search content favorites on social medias.

We offer 2 parts of API's:

* [Users API](/docs/users/index.md) is for existing Likeastore users who wants to access their data and other Likeastore features.
* [Consumers API](/docs/consumers/index.md) is for 3rd parties that want to collect social medias favorites for their own user.

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

## Use cases

* [Likeastore integration use case](/docs/usecase.md)

All questions please forward to [devs@likeastore.com](mailto:devs@likeastore.com).

# License

The MIT License (MIT)

Copyright (c) 2014 Likeastore info@likeastore.com

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.