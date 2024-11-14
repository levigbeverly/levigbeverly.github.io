---
layout: page
---

# `venues` resource

## Base endpoint

```shell
{base_url}/venues
```

## Description

Contains information about each venue created and stored in **Local-Show-Tive**.

## Resource properties

The `venues` resource provides the following information for each venue:

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `name` | string | The name of the venue. |
| `city` | string | The city and state the venue is located in. |
| `venue type` | string | Indicates whether the venue is indoor or outdoor. |
| `age restriction` | string | Indicates whether the venue has an age restriction. |
| `id` | integer | The venue id. This id is used to specify the venue in `concerts` responses. |

## Example `venues` property

```js
{
    "name": "The Depot",
    "city": "South Salt Lake, UT",
    "venue type": "indoor",
    "age restriction": "21+",
    "id": 1
}
```

## Learn more

Use the following links to learn more about the `venues` resource and the API calls you can make to it:
- [Add venue](post-add-venue.md)
- [Update venue](put-update-venue.md)
- [Get venues](get-venues.md)
  - [Get venue details](get-venue-details.md)
  - [Get venue by name](get-venue-by-name.md)
  - [Get venues by city](get-venues-by-city.md)
- [Delete venue](delete-venue.md)
