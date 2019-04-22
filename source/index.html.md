---
title: Bypass Mobile APIs

language_tabs: # must be one of https://git.io/vQNgJ
  - shell: cURL
  - javascript

toc_footers:
  - <a href='https://www.bypassmobile.com/'>Bypass Mobile Home</a>

includes:
  - remoteordering
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

## API Key

Bypass uses API keys to allow access to our services. You can request an API key from Bypass at [Bypass Mobile](https://www.bypassmobile.com/). Bypass requires a valid API key to be included in all API requests to the server in a header that looks like the following:

<aside class="notice">
You must replace <code>bypass</code> with your registered API key.
</aside>

## JWT Token

Authenticating to the REST API requires generating a JWT, or Java Web Token. For more information around JWTs, see this link: [JWT Tokens](https://jwt.io/introduction/).

Internally, we refer to capturing and refreshing JWTs as “BIDM” or “Bypass Identity Management” – so if you see or hear reference to BIDM, they are talking about authenticating a device via a JWT (as opposed to a simple username/password combo).