---
layout: page
---

# Get concerts

## Base endpoint

```shell
{base_url}/concerts
```

## Description

Returns an array of [`concerts`](concerts.md) objects. The array contains all concerts that have been created with **Local-Show-Tive**.

`Get concerts` does not have a request body, parameters, or headers.

## Return body example

The following example of `Get concerts` returns an array containing five concerts:

```js
"concerts": 
[
  {
    "venue_id": 2,
    "artist": "Tank & The Bangas",
    "date": "2025-01-18",
    "time": "8:00PM MST",
    "ticket price": "$32",
    "id": 1
  },
  {
    "venue_id": 1,
    "artist": "JJ Grey & Mofro",
    "date": "2025-01-29",
    "time": "7:00PM MST",
    "ticket price": "N/A",
    "id": 2
  },
  {
    "venue_id": 3,
    "artist": "Lord Huron",
    "date": "2025-05-31",
    "time": "7:00PM MST",
    "ticket price": "$129",
    "id": 3
  },
  {
    "venue_id": 1,
    "artist": "They Might Be Giants",
    "date": "2025-06-10",
    "time": "7:00PM MST",
    "ticket price": "$55",
    "id": 4
  },
  {
    "venue_id": 4,
    "artist": "Joy Oladokun",
    "date": "2025-03-03",
    "time": "8:00PM MST",
    "ticket price": "$26",
    "id": 5
  }
]

```

## Return properties

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `venue_id` | integer | The `venue_id` the concert is taking place at. |
| `artist` | string | The artist performing at the concert. |
| `date` | string | The date the concert takes place on, in `YYYY-MM-DD` format. |
| `time` | string | The time the concert takes place at. The property includes the time zone. |
| `ticket price` | string | The concert ticket price. |
| `id` | integer | The concert id. |

## Return statuses

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Request successful. The server has responded as required. |
| 404 | Error | Requested resource could not be found. |