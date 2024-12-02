---
layout: page
---

# `concerts` resource

## Base endpoint

```shell
{base_url}/concerts
```

## Description

Contains information about each concert created and stored in **Local-Show-Tive**.

## Resource properties

The `concerts` resource provides the following information for each concert:

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `venue_id` | integer | The `venue_id` the concert is taking place at. |
| `artist` | string | The artist performing at the concert. |
| `date` | string | The date the concert takes place on, in `YYYY-MM-DD` format. |
| `time` | string | The time the concert takes place at. The property includes the time zone. |
| `ticket price` | string | The concert ticket price. |
| `id` | integer | The concert id. |

## Example `concerts` property

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

## Learn more

Use the following links to learn more about the `concerts` resource and the API calls you can make to it:
- [Add concert](post-add-concert.md)
- [Update concertr](put-update-concert.md)
- [Get concerts](get-concerts.md)
  - [Get concert details](get-concert-details.md)
  - [Get concerts by artist](get-concerts-by-artist.md)
  - [Get concerts by date](get-concerts-by-date.md)
  - [Get concerts by venue id](get-concerts-by-venue-id.md)
- [Delete concert](delete-concert.md)
