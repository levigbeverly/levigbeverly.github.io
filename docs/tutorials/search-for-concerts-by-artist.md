---
layout: page
---

# Tutorial: Search for concerts by artist

Use the following steps to search for concerts scheduled for a specific artist in **Local-Show-Tive**. You can perform these steps using [cURL commands](#search-for-concerts-by-artist-with-curl-commands) or in the [Postman application](#search-for-concerts-by-artist-in-postman).

You will have to use a command-line tool to complete the tutorial. If you are a first-time user, we recommend using Git Bash. If you use a different command-line tool, you may need to adapt the provided syntax for your tool of choice.

The tutorial will take about five minutes. 

_**Note:** This tutorial assumes that you have already completed the **Local-Show-Tive** getting started process. If you have not, complete the steps described in [Getting started](../getting-started.md), then return to this tutorial._

## Search for concerts by artist with cURL commands

1. In your preferred command line tool, start **Local-Show-Tive** locally by entering the following command:

    ```shell
    cd <your-github-workspace>/local-show-tive/api
    json-server -w local-show-tive-source.json
    ```
    You must keep this window open for the remainder of the process.

2. In a separate window of your command line tool, enter in the following GET command to retrieve a list of concerts taking place for a specific artist. For this example, we will use `Periphery` as the example artist.

    ```shell
    curl {base_url}/concerts?artist=Periphery
    ```
    _**Note:** When run locally for testing, the `{base_url}` is generally `http://localhost:3000`._

    You can change the `artist` value as you see fit. For more information, see the [Get concerts by artist reference](../references/get-concerts-by-artist.md).
    
    The response message lists every `Periphery` concert in **Local-Show-Tive**.

3. To locate where a specific concert is taking place, looking at the response message, identify the concert that you are interested in and record its `venue_id`. 
    
    For this example, we will search for a concert with a `venue_id` of `2`. 

4. Type in the following GET command to search for the venue with a `venue_id` of `2`:

    ```shell
    curl {base_url}/venues?id=2
    ```
    _**Note:** When run locally for testing, the `{base_url}` is generally `http://localhost:3000`._

   You can change the `id` value as you see fit. For more information, see the [Get venue by id reference](../references/get-venue-by-id.md).

   The response message lists the venue with an `id` of `2`:

   ```js
   [
        {
            "name": "The Commonwealth Room",
            "city": "Salt Lake City, UT",
            "venue type": "indoor",
            "age restriction": "21+",
            "id": 2
        }
    ]
   ```

## Search for concerts by artist in Postman

1. In your preferred command line tool, start **Local-Show-Tive** locally by entering the following command:

    ```shell
    cd <your-github-workspace>/local-show-tive/api
    json-server -w local-show-tive-source.json
    ```
    You must keep this window open for the remainder of the process.

2. Open the Postman app.

3. Create the following GET command to retrieve a list of concerts taking place for a specific artist. For this example, we will use `Periphery` as the example artist.

    ```shell
    GET {base_url}/concerts?artist=Periphery
    ```
    _**Note:** When run locally for testing, the `{base_url}` is generally `http://localhost:3000`._

4. Click **Send**.

   The response message lists every Periphery concert in **Local-Show-Tive**.

5. Identify the venue that you want to search concerts for by recording the venue's `id`. You will need the `id` for step 6.

   For this example, we will search for a concert with a `venue_id` of `2`. 

6. Create the following GET command to search for the venue with a `venue_id` of `2`:

    ```shell
    GET {base_url}/venues?id=2
    ```
    _**Note:** When run locally for testing, the `{base_url}` is generally `http://localhost:3000`._

7. Click **Send**. 

   Postman returns a `200 OK` message and lists the venue with an `id` of `2`:

   ```js
   [
        {
            "name": "The Commonwealth Room",
            "city": "Salt Lake City, UT",
            "venue type": "indoor",
            "age restriction": "21+",
            "id": 2
        }
    ]
   ```

## Related tutorials

For more concert tutorials, see the following topics:
- [Add a concert](add-a-concert.md)
- [Change a concert's date and time](change-a-concerts-date-and-time.md)
- [Search for concerts by venue](search-for-concerts-by-venue.md)
- [Delete a concert](delete-a-concert.md)