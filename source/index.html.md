---
title: Storydoc API Reference

language_tabs:
  - shell

toc_footers:
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Storydoc API! You can use our API to access Storydoc API endpoints.

We have language bindings in Shell! You can view code examples in the dark area to the right.

# Authentication

> To authorize, use this code:

```shell
# With shell, you can just pass the username and password with each request
curl "https://user:pass@storydoc-api-stg.mybluemix.net/users/me"
```

> Make sure to replace `user` and `pass` with your email address and password.

Storydoc expects for the authentication to be included in all API requests to the server, using the username and password. Once authorized, the endpoint will return a token that can be used instead of the password for future calls.

# Users

## Get All Users


```shell
curl "https://user:pass@storydoc-api-stg.mybluemix.net/users"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "email": 'vincent@storydoc.ai',
    "password": '123456',
    "name": 'Vincent',
    "permissionLevel": 100,
    "status": 1,
    "accountId": 0,
    "profession": 'Doctor',
    "phoneNumber": '555-555-5555',
    "picture": '',
    "dateCreated": '2017-04-18 23:59:00',
    "dateUpdated": '2017-04-18 23:59:00'
  },
  {
    "id": 2,
    "email": 'client@storydoc.ai',
    "password": '123456',
    "name": 'Vincent',
    "permissionLevel": 50,
    "status": 1,
    "accountId": 1,
    "profession": 'Client',
    "phoneNumber": '555-555-5555',
    "picture": '',
    "dateCreated": '2017-04-18 23:59:00',
    "dateUpdated": '2017-04-18 23:59:00'
  }
]
```

This endpoint retrieves all users.

### HTTP Request

`GET https://storydoc-api-stg.mybluemix.net/users`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
filter | [] | If defined, will filter the results.
sort | [] | If defined, will sort the results.
page | 0 | Starting at the page.
perPage | 30 | The number of items per page.

## Get a Specific User

```shell
curl "https://user:pass@storydoc-api-stg.mybluemix.net/users/1"
```

> The above command returns JSON structured like this:

```json
{
  "id": 1,
  "email": 'vincent@storydoc.ai',
  "password": '123456',
  "name": 'Vincent',
  "permissionLevel": 100,
  "status": 1,
  "accountId": 0,
  "profession": 'Doctor',
  "phoneNumber": '555-555-5555',
  "picture": '',
  "dateCreated": '2017-04-18 23:59:00',
  "dateUpdated": '2017-04-18 23:59:00'
}
```

This endpoint retrieves a specific user.

### HTTP Request

`GET https://storydoc-api-stg.mybluemix.net/users/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the user to retrieve

## Create a User

### HTTP Request

`POST https://storydoc-api-stg.mybluemix.net/users`

## Update a User

### HTTP Request

`PUT https://storydoc-api-stg.mybluemix.net/users/<ID>`

## Delete a User

### HTTP Request

`DELETE https://storydoc-api-stg.mybluemix.net/users/<ID>`


# Accounts

## Get All Accounts

### HTTP Request

`GET https://storydoc-api-stg.mybluemix.net/accounts`

## Get a Specific Account

### HTTP Request

`GET https://storydoc-api-stg.mybluemix.net/accounts/<ID>`

## Create a Account

### HTTP Request

`POST https://storydoc-api-stg.mybluemix.net/accounts`

## Update a Account

### HTTP Request

`PUT https://storydoc-api-stg.mybluemix.net/accounts/<ID>`

## Delete a Account

### HTTP Request

`DELETE https://storydoc-api-stg.mybluemix.net/accounts/<ID>`


# Stories

## Get All Accounts

### HTTP Request

`GET https://storydoc-api-stg.mybluemix.net/accounts`

## Get a Specific Account

### HTTP Request

`GET https://storydoc-api-stg.mybluemix.net/accounts/<ID>`

## Create a Account

### HTTP Request

`POST https://storydoc-api-stg.mybluemix.net/accounts`

## Update a Account

### HTTP Request

`PUT https://storydoc-api-stg.mybluemix.net/accounts/<ID>`

## Delete a Account

### HTTP Request

`DELETE https://storydoc-api-stg.mybluemix.net/accounts/<ID>`


# Nodes

## Get All Nodes

### HTTP Request

`GET https://storydoc-api-stg.mybluemix.net/nodes`

## Get a Specific Node

### HTTP Request

`GET https://storydoc-api-stg.mybluemix.net/nodes/<ID>`

## Create a Node

### HTTP Request

`POST https://storydoc-api-stg.mybluemix.net/nodes`

## Update a Node

### HTTP Request

`PUT https://storydoc-api-stg.mybluemix.net/nodes/<ID>`

## Delete a Node

### HTTP Request

`DELETE https://storydoc-api-stg.mybluemix.net/nodes/<ID>`


# Links

## Get All Links

### HTTP Request

`GET https://storydoc-api-stg.mybluemix.net/links`

## Get a Specific Link

### HTTP Request

`GET https://storydoc-api-stg.mybluemix.net/links/<ID>`

## Create a Link

### HTTP Request

`POST https://storydoc-api-stg.mybluemix.net/links`

## Update a Link

### HTTP Request

`PUT https://storydoc-api-stg.mybluemix.net/links/<ID>`

## Delete a Link

### HTTP Request

`DELETE https://storydoc-api-stg.mybluemix.net/links/<ID>`


# Files

## Create a File

### HTTP Request

`POST https://storydoc-api-stg.mybluemix.net/files`
