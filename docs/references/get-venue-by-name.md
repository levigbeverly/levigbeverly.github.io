---
title: Get venue by name
parent: Venues
nav_order: 5
---

# Get venue by name

## Base endpoint

```shell
{base_url}/venues?name={venue%20name}
```

## Description

Returns details for a venue specified by name. Specify the venue by entering the venue name at the end of the request URL. If the venue name contains spaces, you must fill each space with `%20`.

`Get venue by name` does not have a request body, parameters, or headers.

## Return body example

In this example the user runs the following command:

```shell
{base_url}/venues?name={The%20Depot}
```

**Local-Show-Tive** returns the following message:

```js
{
  "name": "The Depot",
  "city": "South Salt Lake, UT",
  "venue type": "indoor",
  "age restriction": "21+",
  "id": 1
},
```

## Return properties

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `name` | string | The name of the venue. |
| `city` | string | The city and state the venue is located in. |
| `venue type` | string | Indicates whether the venue is indoor or outdoor. |
| `age restriction` | string | Indicates whether the venue has an age restriction. |
| `id` | integer | The venue id. This id is used to specify the venue in `concerts` responses. |

## Return statuses

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Request successful. The server has responded as required. |
| 404 | Error | Requested resource could not be found. ||
