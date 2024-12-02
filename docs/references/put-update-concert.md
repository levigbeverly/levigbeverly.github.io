---
title: Update concert
parent: Concerts
nav_order: 2
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

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `venue_id` | integer | Enter the `venue_id` of the venue the concert is taking place at. |
| `artist` | string | Enter the name of the artist performing at the concert. |
| `date` | string | Enter the date the concert takes place on in `YYYY-MM-DD` format. |
| `time` | string | Enter the time the concert takes place at in the following format: {time}{AM/PM} {abbreviated time zone} (for example, `8:00PM MST`).|
| `ticket price` | string | Enter the concert ticket price in the following format: {currency type}{amount} (for example, `$26`).|

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
