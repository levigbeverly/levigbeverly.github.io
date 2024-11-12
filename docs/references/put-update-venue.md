---
layout: page
---

# Update venue

## Base endpoint

```shell
PUT {base_url}/venues/{id}
```

## Description

Updates an existing `venues` object. Enter the venue information to update in the response body.

## Request properties

You can specify any combination the following venue details in the `Update venue` response body:

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `name` | string | Enter the name of the venue. |
| `city` | string | Enter the city and state (abbreviated) the venue is located in. |
| `type` | string | Indicate whether the venue is indoor or outdoor. The valid options are `indoor` and `outdoor`. |
| `age restriction` | string | Indicate whether the venue has an age restriction. The valid options are `all ages` and `21+`.  |

## Request body example

The following request body example will add a new venue - `The Depot` - to the **Local-Show-Tive** database. The Depot is located in South Salt Lake, UT, is an indoor venue, and has an age restriction of 21+.

```js
{
  "name": "The Depot",
  "city": "South Salt Lake, UT",
  "venue_type": "outdoor",
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
