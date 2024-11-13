---
layout: page
---

# Get concerts by artist

## Base endpoint

```shell
{base_url}/concerts?artist={artist}
```

## Description

Returns details for concerts specified by artist. Specify the concert or concerts by entering the artist name at the end of the request URL. If the artist name contains spaces, you must fill each space with `%20`.

`Get concerts by artist` does not have a request body, parameters, or headers.

## Return body example

In this example, the user runs the following command:

```shell
{base_url}/concerts?artist=Periphery
```

**Local-Show-Tive** returns the following message:

```js
[
  {
    "venue_id": 2,
    "artist": "Periphery",
    "date": "2025-02-21",
    "time": "9:00PM MST",
    "ticket price": "$35",
    "id": 6
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