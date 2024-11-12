---
layout: page
---

# Add concert

## Base endpoint

```shell
POST {base_url}/concerts
```

## Description

Creates a new `concerts` object. Enter the concert information in the request body.

## Request properties

Specify the following venue details in the `Create concert` response body:

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `venue_id` | integer | Enter the `venue_id` of the venue the concert is taking place at. |
| `artist` | string | Entwr the name of the artist performing at the concert. |
| `date` | string | Enter the date the concert takes place on in `YYYY-MM-DD` format. |
| `time` | string | Enter the time the concert takes place at in the following format: {time}{AM/PM} {abbreviated time zone} (for example, `8:00PM MST`).|
| `ticket price` | string | Enter the concert ticket price in the following format: {currency type}{amount} (for example, `$26`).|

## Request body example

The following request body example will add a new concert to the **Local-Show-Tive** database. The concert is held at the `venues` object whose `id` is `4`. The artist performing is Joy Oladokun, the concert takes place on March 3, 2025 at 8:00PM MST, and the ticket price is $26.

```js
  {
    "venue_id": 4,
    "artist": "Joy Oladokun",
    "date": "2025-03-03",
    "time": "8:00PM MST",
    "ticket price": "$26",
  }

```

## Return body example

The following example of `Create concert` returns a confirmation that the new concert was created:

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
