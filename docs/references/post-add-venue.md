---
layout: page
---

# Add venue

## Base endpoint

```shell
POST {base_url}/venues
```

## Description

Creates a new `venues` object. Enter the venue name and related information in the request response body.

## Request body

Specify the following venue details in the `Create venue` response body:



## Request body example

The following request body example will add a new venue - `The Depot`, and it's basic information - to the **Local-Show-Tive** database:

```js
{
  "name": "The Depot",
  "city": "South Salt Lake, UT",
  "venue_type": "indoor",
  "age_restriction": "21+",
  "id": 1
}

```

## Return body example

The following example of `Create venue` returns a confirmation that the new venue was created:

```js
{
  "message": "Resource created successfully."
}

```

## Return statuses

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Request successful. The server has responded as required. |
| 404 | Error | Requested resource could not be found. |
