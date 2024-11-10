---
layout: page
---
# Local-Show-Tive

**Local-Show-Tive** is a REST API service that makes local concert planning and searching easy and streamlined. 
- _Concert-goers_: You can use **Local-Show-Tive** to find a detailed list of upcoming shows in your area.
- _Venue owners_: You can use **Local-Show-Tive** to share consistent information about your venue.
- _Artists, managers_, and promoters: You can use **Local-Show-Tive** to post and update information about your upcoming shows

**Local-Show-Tive** allows users to update and query an ongoing database of live music events. 

**Local-Show-Tive** is cloud-based and available for use on any device that can connect to the internet. The service is easy to use, and requires minimal to no experience with REST APIs. 

## First-time Users

If this is your first time setting up and using **Local-Show-Tive**, see [Getting Started](getting-started.md). The topic walks you through the service prerequisites and how to set up the service.

## Tutorials

Learn how to do the most common **Local-Show-Tive** tasks:
 - [Add a venue](tutorials/add-a-venue.md)
 - [Add a concert](tutorials/add-a-concert.md)
 - [Search for concerts by venue](tutorials/)
 - [Search for concerts by artist](tutorials/)

To view the full list of available tutorials, click **Tutorials** below:
<details>
  <summary>Tutorials</summary>
  
  - **venues**
    - [Add a venue](tutorials/add-a-venue.md)
    - [Update a venue](tutorials/update-a-venue.md)
    - [Delete a venue](tutorials/delete-a-venue.md)
 
  - **concerts**
    - [Add a concert](tutorials/add-a-concert.md)
    - [Change a concert's date and time](tutorials/change-a-concerts-date-and-time.md)
    - [Search for concerts by venue](tutorials/search-for-concerts-by-venue.md)
    - [Search for concerts by artist](tutorials/search-for-concerts-by-artist.md)
    - [Delete a concert](tutorials/delete-a-concert.md)
</details>

## References

All show-related actions are performed under the [`shows`]() resource, and all venue-related actions are performed with the [`venues`]() resource.

To view detailed descriptions the service's resources and individual API calls, click **References** below:
<details>
  <summary>References</summary>
  
  - [**venues** resource](references/venues.md)
    - **POST**
      - [Add venue](references/post-add-venue.md)
    - **PUT**
      - [Update venue](references/put-update-venue.md)
    - **GET**
      - [Get venues](references/get-venues.md)
      - [Get venue by name](references/get-venue-by-name.md)
      - [Get venue by id](references/get-venue-by-id.md)
      - [Get venue by city](references/get-venue-by-city.md)
    - **DELETE**
      - [Delete venue](references/delete-venue.md)

  - [**concerts** resource](references/concerts.md)
    - **POST**
      - [Add concert](references/post-add-concert.md)
    - **PUT**
      - [Update concert](references/put-update-concert.md)
    - **GET**
      - [Get concerts](references/get-concerts.md)
      - [Get concert by venue id](references/get-concert-by-venue-id.md)
      - [Get concert by artist](references/get-concert-by-artist.md)
      - [Get concert by date](references/get-concert-by-date.md)
    - **DELETE**
      - [Delete concert](references/delete-concert.md)
</details>

## Contact Us

If you have questions or inquiries related to **Local-Show-Tive** or its documentation, please email `levigbeverly@gmail.com`.
