---
title: Bypass Mobile API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - ruby
  - python
  - javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the ByPass Mobile API! You can use our API to access the Mobile Ordering API endpoints. It is assumed that we will be sent a valid user identifier.

# Authentication

> To authorize, use this code:

```ruby
require 'bpm'

api = bpm::APIClient.authorize!('bypass')
```

```python
import bpm

api = bpm.authorize('bypass')
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: bypass"
```

```javascript
const bpm = require('bpm');

let api = bpm.authorize('bypass');
```

> Make sure to replace `bypass` with your API key.

bpm uses API keys to allow access to the API. You can register a new bpm API key at our [developer portal](http://example.com/developers).

bpm expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: bypass`

<aside class="notice">
You must replace <code>bypass</code> with your personal API key.
</aside>

# Kittens

## Get All Kittens

```ruby
require 'bpm'

api = bpm::APIClient.authorize!('bypass')
api.kittens.get
```

```python
import bpm

api = bpm.authorize('bypass')
api.kittens.get()
```

```shell
curl "http://example.com/api/kittens"
  -H "Authorization: bypass"
```

```javascript
const bpm = require('bpm');

let api = bpm.authorize('bypass');
let kittens = api.kittens.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all kittens.

### HTTP Request

`GET http://example.com/api/kittens`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a Specific Kitten

```ruby
require 'bpm'

api = bpm::APIClient.authorize!('bypass')
api.kittens.get(2)
```

```python
import bpm

api = bpm.authorize('bypass')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -H "Authorization: bypass"
```

```javascript
const bpm = require('bpm');

let api = bpm.authorize('bypass');
let max = api.kittens.get(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

## Delete a Specific Kitten

```ruby
require 'bpm'

api = bpm::APIClient.authorize!('bypass')
api.kittens.delete(2)
```

```python
import bpm

api = bpm.authorize('bypass')
api.kittens.delete(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -X DELETE
  -H "Authorization: bypass"
```

```javascript
const bpm = require('bpm');

let api = bpm.authorize('bypass');
let max = api.kittens.delete(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific kitten.

### HTTP Request

`DELETE http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to delete

