---
layout: page
---

# Get venues

## Base endpoint

```shell
{base_url}/venues
```

## Description

Returns an array of [`venues`](venues.md) objects. The array contains all venues that have been created with Local-Show-Tive.

`Get venues` does not have a request body, parameters, or headers.

## Return body example

The following example of **Get venues** returns an array containing four venues:

```js
"venues": [
    {
      "name": "The Depot",
      "city": "South Salt Lake, UT",
      "venue type": "indoor",
      "age restriction": "21+",
      "id": 1
    },
    {
      "name": "The Commonwealth Room",
      "city": "Salt Lake City, UT",
      "venue type": "indoor",
      "age restriction": "21+",
      "id": 2
    },
    {
      "name": "Sandy Amphitheater",
      "city": "Sandy, UT",
      "venue type": "outdoor",
      "age restriction": "all ages",
      "id": 3
    },
    {
      "name": "Soundwell",
      "city": "Salt Lake City, UT",
      "type": "indoor",
      "age restriction": "all ages",
      "id": 4
    }
  ]

```

## Return properties

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `name` | string | The name of the venue. |
| `city` | string | The city and state the venue is located in. |
| `type` | string | Indicates whether the venue is indoor or outdoor. |
| `age restriction` | string | Indicates whether the venue has an age restriction. |
| `id` | integer | The venue id. This id is used to specify the venue in `concerts` responses. |


## Return statuses

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Request successful. The server has responded as required. |
| 404 | Error | Requested resource could not be found. |
