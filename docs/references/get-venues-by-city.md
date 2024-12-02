---
title: Get venue by city
parent: Venues
nav_order: 6
---

# Get venue by city

## Base endpoint

```shell
{base_url}/venues?city={city%20name,%20state}
```

## Description

Returns details for a venue specified by name. Specify the venue by entering the venue name at the end of the request URL. When specifying the city, you must include the state abbreviation, fill every space with `%20`, and replace any commas with `%2C`.

`Get venue by city` does not have a request body, parameters, or headers.

## Return body example

In this example the user runs the following command:

```shell
{base_url}/venues?city={South%20Salt%20Lake%2C%20UT}
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
