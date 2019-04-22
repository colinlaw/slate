# Remote Ordering API

The remote ordering API enables a 3rd party to generate a context call which is the base for accessing locations and menus. A 3rd party with location and menu access can create orders, send order payments and refund orders.

## Context
All of the context required by a client application to make decisions on subsequent calls.

### Get Context
<aside class="notice">https://mobile-ordering.bypassmobile.com/context</aside>

The successful result of the context call.

**Model**


<table class="tables">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>venue_id</td>
<td>number</td>
<td>The Bypass venue_id</td>
</tr>
<tr>
<td>session_token</td>
<td>string</td>
<td>The session token to be used against the gateway</td>
</tr>
<tr>
<td>gateway_url</td>
<td>string</td>
<td>The url to use for credit card tokenization</td>
</tr>
</tbody>
</table>


**`HEADERS`**

**X-USER-ID** 6592cf35ce308d81a78d5133f8faa29a

**X-VENUE-ID** 1068

```shell
curl -X GET \
  https://mobile-ordering.bypassmobile.com/context \
  -H 'Postman-Token: 905c6dff-ab76-451d-a12c-a41e186a3f71' \
  -H 'X-USER-ID: 6592cf35ce308d81a78d5133f8faa29a' \
  -H 'X-VENUE-ID: 1068' \
  -H 'cache-control: no-cache'
```

```javascript
var form = new FormData();
var settings = {
  "url": "https://mobile-ordering.bypassmobile.com/context",
  "method": "GET",
  "timeout": 0,
  "headers": {
    "X-USER-ID": "6592cf35ce308d81a78d5133f8faa29a",
    "X-VENUE-ID": "1068"
  },
  "processData": false,
  "mimeType": "multipart/form-data",
  "contentType": false,
  "data": form
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

> The above command returns JSON structured like this:

```json
{
    "venue_id": 1068,
    "session_token": "49b94fc08325f92c3a88f8f46fbceb87",
    "gateway_url": "https://zuul.bypassmobile.com"
}
```

# Locations

## Get Locations

# Venues

## Get Venues

# Orders

## Create Order

# Wallet

## Add Wallet