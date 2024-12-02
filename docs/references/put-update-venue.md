---
title: Update venue
parent: Venues
nav_order: 2
---

# Update venue

## Base endpoint

```shell
PUT {base_url}/venues/{id}
```

## Description

Updates an existing `venues` object. Specify the venue to update by entering the venue id at the end of the request URL.

Enter the venue information to update in the response body.

## Request properties

You can specify any combination the following venue details in the `Update venue` response body:

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `name` | string | Enter the name of the venue. |
| `city` | string | Enter the city and state (abbreviated) the venue is located in. |
| `type` | string | Indicate whether the venue is indoor or outdoor. The valid options are `indoor` and `outdoor`. |
| `age restriction` | string | Indicate whether the venue has an age restriction. The valid options are `all ages` and `21+`.  |

## Request body example

The following request body example will update the specified venue with a venue type of `outdoor`:

```js
{
  "venue type": "outdoor"
}

```

## Return body example

The following example of `Update venue` returns a confirmation that the new venue was updated:

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
