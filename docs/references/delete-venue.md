---
title: Delete venue
parent: Venues
nav_order: 3
---

# Delete venue

## Base endpoint

```shell
DELETE {base_url}/venues/{id}
```

## Description

Deletes the specified `venues` object. Specify the venue to delete by entering the venue `id` at the end of the request URL.

`Delete venue` does not have a request body, parameters, or headers.

## Return body example

The following example of `Delete venue` returns a confirmation that the specified venue was deleted:

```js
{
  "message": "Resource deleted successfully."
}

```

## Return statuses

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Request successful. The server has responded as required. |
| 404 | Error | Requested resource could not be found. |
