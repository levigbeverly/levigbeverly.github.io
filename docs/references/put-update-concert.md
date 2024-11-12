---
layout: page
---

# Update concert

## Base endpoint

```shell
PUT {base_url}/concerts/{id}
```

## Description

Updates an existing `concerts` object. Specify the concert to update by entering the concert id at the end of the request URL.

Enter the concert information to update in the response body.

## Request properties

You can specify any combination the following concert details in the `Update concert` response body:



## Request body example

The following request body example will update the specified concert with a date of `2025-05-10`:

```js
{
  "date": "2025-05-10"
}

```

## Return body example

The following example of `Update concert` returns a confirmation that the new venue was updated:

```js
{
  "message": "Resource updated successfully."
}

```

## Return statuses

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Request successful. The server has responded as required. |
| 404 | Error | Requested resource could not be found. |
