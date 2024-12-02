---
title: Get venue details
parent: Venues
nav_order: 4
---

# Get venue details

## Base endpoint

```shell
{base_url}/venues/{id}
```

## Description

Returns details for a specified venue. Specify the venue by entering the venue id at the end of the request URL.

`Get venue details` does not have a request body, parameters, or headers.

## Return body example

In this example the user runs the following command:

```shell
{base_url}/venues/1
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
| 404 | Error | Requested resource could not be found. |
