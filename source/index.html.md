---
title: Bypass Mobile APIs

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - ruby
  - python
  - javascript

toc_footers:
  - <a href='https://www.bypassmobile.com/'>Bypass Mobile Home</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the ByPass Mobile APIs! You can use our APIs as a Collection of API calls to interact with Remote Ordering, Promotions and Stored Value.

Bypass offers 3 API services that are accessed via a Proxy.

**Remote Ordering:** The remote ordering API enables a 3rd party to generate a context call which is the base for accessing locations and menus. A 3rd party with location and menu access can create orders, send order payments and refund orders.

**Promotions:** The promotions API allows a 3rd party to attach a promotion sych as 10% off an order when a promotion has been enabled by a customer for their location.

**Stored Value:** The SV API provides a 3rd party with access to our integrated SV providers. With this services, you can check balances, redeem funds, add funds, activate cards, refund payments and manage accounts.

**Note:** To process payments, you are required to tokenize a credit card. There is an example call to demonstrate how this call is performed.

# Foundation

## JWT Tokens
## API Keys
## URLs
## Venues
## Locations
## Menus

# Authentication

## JWT Token

## API Key

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

Bypass uses API keys to allow access to our services. You can request an API key from Bypass at [Bypass Mobile](https://www.bypassmobile.com/).

Bypass requires a valid API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: bypass`

<aside class="notice">
You must replace <code>bypass</code> with your registered API key.
</aside>

# Remote Ordering API

## Context

### Get Context

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

# Locations

## Get Locations

# Venues

## Get Venues

# Orders

## Create Order

# Wallet

## Add Wallet