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
  
<ul>
  <li><strong>venues</strong>
    <ul>
      <li><a href="tutorials/add-a-venue.md">Add a venue</a></li>
      <li><a href="tutorials/update-a-venue.md">Update a venue</a></li>
      <li><a href="tutorials/delete-a-venue.md">Delete a venue</a></li>
    </ul>
  </li>
  
  <li><strong>concerts</strong>
    <ul>
      <li><a href="tutorials/add-a-concert.md">Add a concert</a></li>
      <li><a href="tutorials/change-a-concerts-date-and-time.md">Change a concert's date and time</a></li>
      <li><a href="tutorials/search-for-concerts-by-venue.md">Search for concerts by venue</a></li>
      <li><a href="tutorials/search-for-concerts-by-artist.md">Search for concerts by artist</a></li>
      <li><a href="tutorials/delete-a-concert.md">Delete a concert</a></li>
    </ul>
  </li>
</ul>

</details>

## References

All show-related actions are performed under the [`shows`]() resource, and all venue-related actions are performed with the [`venues`]() resource.

To view detailed descriptions the service's resources and individual API calls, click **References** below:
<details>
  <summary>References</summary>
  
<ul>
  <li><a href="references/venues.md"><strong>venues</strong> resource</a>
    <ul>
      <li><strong>POST</strong>
        <ul>
          <li><a href="references/post-add-venue.md">Add venue</a></li>
        </ul>
      </li>
      <li><strong>PUT</strong>
        <ul>
          <li><a href="references/put-update-venue.md">Update venue</a></li>
        </ul>
      </li>
      <li><strong>GET</strong>
        <ul>
          <li><a href="references/get-venues.md">Get venues</a></li>
          <li><a href="references/get-venue-by-name.md">Get venue by name</a></li>
          <li><a href="references/get-venue-by-id.md">Get venue by id</a></li>
          <li><a href="references/get-venue-by-city.md">Get venue by city</a></li>
        </ul>
      </li>
      <li><strong>DELETE</strong>
        <ul>
          <li><a href="references/delete-venue.md">Delete venue</a></li>
        </ul>
      </li>
    </ul>
  </li>
  
  <li><a href="references/concerts.md"><strong>concerts</strong> resource</a>
    <ul>
      <li><strong>POST</strong>
        <ul>
          <li><a href="references/post-add-concert.md">Add concert</a></li>
        </ul>
      </li>
      <li><strong>PUT</strong>
        <ul>
          <li><a href="references/put-update-concert.md">Update concert</a></li>
        </ul>
      </li>
      <li><strong>GET</strong>
        <ul>
          <li><a href="references/get-concerts.md">Get concerts</a></li>
          <li><a href="references/get-concert-by-venue-id.md">Get concert by venue id</a></li>
          <li><a href="references/get-concert-by-artist.md">Get concert by artist</a></li>
          <li><a href="references/get-concert-by-date.md">Get concert by date</a></li>
        </ul>
      </li>
      <li><strong>DELETE</strong>
        <ul>
          <li><a href="references/delete-concert.md">Delete concert</a></li>
        </ul>
      </li>
    </ul>
  </li>
</ul>

</details>

## Contact Us

If you have questions or inquiries related to **Local-Show-Tive** or its documentation, please email `levigbeverly@gmail.com`.
