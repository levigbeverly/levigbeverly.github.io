---
layout: page
---

# Delete concert

## Base endpoint

```shell
DELETE {base_url}/concerts/{id}
```

## Description

Deletes the specified `concerts` object. Specify the concert to delete by entering the concert `id` at the end of the request URL.

`Get concerts` does not have a request body, parameters, or headers.

## Return body example

The following example of `Delete concert` returns a confirmation that the specified concert was deleted:

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
