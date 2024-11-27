---
layout: page
---
# Local-Show-Tive

**Local-Show-Tive** is a REST API service that makes local concert planning and searching in the US easy and streamlined. 
- _Concert-goers_: You can use **Local-Show-Tive** to find a detailed list of upcoming shows in your area.
- _Venue owners_: You can use **Local-Show-Tive** to share consistent information about your venue.
- _Artists, managers, and promoters_: You can use **Local-Show-Tive** to post and update information about your upcoming shows.

**Local-Show-Tive** allows users to update and query an ongoing database of live music events. 

**Local-Show-Tive** is cloud-based and available for use on any device that can connect to the internet. The service is easy to use, and requires minimal to no experience with REST APIs. 

## First-time Users

If this is your first time setting up and using **Local-Show-Tive**, see [Getting Started](getting-started.md). The topic walks you through the service prerequisites and how to test the service on your machine.

Once you complete the Getting Started process, see [Quickstart](quickstart.md) to quickly set up your first concerts and venues.

## Tutorials

Learn how to do the most common **Local-Show-Tive** tasks:
 - [Add a venue](tutorials/add-a-venue.html)
 - [Add a concert](tutorials/add-a-concert.html)
 - [Search for concerts by venue](tutorials/search-for-concerts-by-venue.html)
 - [Search for concerts by artist](tutorials/search-for-concerts-by-artist.html)

To view the full list of available tutorials, click **Tutorials** below:
<details>
  <summary>Tutorials</summary>
  
<ul>
  <li><strong>venues</strong>
    <ul>
      <li><a href="tutorials/add-a-venue.html">Add a venue</a></li>
      <li><a href="tutorials/update-a-venue.html">Update a venue</a></li>
      <li><a href="tutorials/delete-a-venue.html">Delete a venue</a></li>
    </ul>
  </li>
  
  <li><strong>concerts</strong>
    <ul>
      <li><a href="tutorials/add-a-concert.html">Add a concert</a></li>
      <li><a href="tutorials/update-a-concert.html">Update a concert</a></li>
      <li><a href="tutorials/search-for-concerts-by-venue.html">Search for concerts by venue</a></li>
      <li><a href="tutorials/search-for-concerts-by-artist.html">Search for concerts by artist</a></li>
      <li><a href="tutorials/delete-a-concert.html">Delete a concert</a></li>
    </ul>
  </li>
</ul>

</details>

## References

All venue-related actions are performed under the [`venues`](references/venues.md) resource, and all concert-related actions are performed with the [`concerts`](references/concerts.md) resource.

To view detailed descriptions the service's resources and individual API calls, click **References** below:
<details>
  <summary>References</summary>
  
<ul>
  <li><a href="references/venues.html"><strong>venues</strong></a> resource
    <ul>
      <li><strong>POST</strong>
        <ul>
          <li><a href="references/post-add-venue.html">Add venue</a></li>
        </ul>
      </li>
      <li><strong>PUT</strong>
        <ul>
          <li><a href="references/put-update-venue.html">Update venue</a></li>
        </ul>
      </li>
      <li><strong>GET</strong>
        <ul>
          <li><a href="references/get-venues.html">Get venues</a></li>
          <li><a href="references/get-venue-details.html">Get venue details</a></li>
          <li><a href="references/get-venue-by-name.html">Get venue by name</a></li>
          <li><a href="references/get-venues-by-city.html">Get venues by city</a></li>
        </ul>
      </li>
      <li><strong>DELETE</strong>
        <ul>
          <li><a href="references/delete-venue.html">Delete venue</a></li>
        </ul>
      </li>
    </ul>
  </li>
  
  <li><a href="references/concerts.html"><strong>concerts</strong></a> resource
    <ul>
      <li><strong>POST</strong>
        <ul>
          <li><a href="references/post-add-concert.html">Add concert</a></li>
        </ul>
      </li>
      <li><strong>PUT</strong>
        <ul>
          <li><a href="references/put-update-concert.html">Update concert</a></li>
        </ul>
      </li>
      <li><strong>GET</strong>
        <ul>
          <li><a href="references/get-concerts.html">Get concerts</a></li>
          <li><a href="references/get-concert-details.html">Get concert details</a></li>
          <li><a href="references/get-concerts-by-venue-id.html">Get concerts by venue id</a></li>
          <li><a href="references/get-concerts-by-artist.html">Get concerts by artist</a></li>
          <li><a href="references/get-concerts-by-date.html">Get concerts by date</a></li>
        </ul>
      </li>
      <li><strong>DELETE</strong>
        <ul>
          <li><a href="references/delete-concert.html">Delete concert</a></li>
        </ul>
      </li>
    </ul>
  </li>
</ul>

</details>

## Contact Us

If you have questions or inquiries related to **Local-Show-Tive** or its documentation, please email `levigbeverly@gmail.com`.
