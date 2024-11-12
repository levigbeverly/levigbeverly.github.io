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

## Request properties

Specify the following venue details in the `Create venue` response body:

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `name` | string | Enter the name of the venue. |
| `city` | string | Enter the city and state (abbreviated) the venue is located in. |
| `type` | string | Indicate whether the venue is indoor or outdoor. The valid options are `indoor` and `outdoor`. |
| `age restriction` | string | Indicate whether the venue has an age restriction. The valid options are  |
| `id` | integer | The venue id. This id is used to specify the venue in `concerts` responses. |

## Request body example

The following request body example will add a new venue - `The Depot`, and it's basic information - to the **Local-Show-Tive** database. The service automatically assigns the venue with an `id` of `5`.

```js
{
  "name": "The Depot",
  "city": "South Salt Lake, UT",
  "venue_type": "indoor",
  "age_restriction": "21+",
  "id": 5
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
