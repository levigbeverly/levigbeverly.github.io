---
layout: page
---

# Get concert details

## Base endpoint

```shell
{base_url}/concerts
```

## Description

Returns details for a specified concert. Specify the concert by entering the concert id at the end of the request URL.

`Get concert details` does not have a request body, parameters, or headers.

## Return body example

In this example, the user runs the following command:

```shell
{base_url}/concerts/1
```

**Local-Show-Tive** returns the following message:

```js
  {
    "venue_id": 2,
    "artist": "Tank & The Bangas",
    "date": "2025-01-18",
    "time": "8:00PM MST",
    "ticket price": "$32",
    "id": 1
  }
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