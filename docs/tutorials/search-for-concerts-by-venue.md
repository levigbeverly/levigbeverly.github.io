---
layout: page
---

# Tutorial: Search for concerts by venue

Use the following steps to search for concerts scheduled for a specific venue in **Local-Show-Tive**. You can perform these steps using [cURL commands](#search-for-concerts-by-venue-with-curl-commands) or in the [Postman application](#search-for-concerts-by-venue-in-postman).

You will have to use a command-line tool to complete the tutorial. If you are a first-time user, we recommend using Git Bash. If you use a different command-line tool, you may need to adapt the provided syntax for your tool of choice.

The tutorial will take about seven minutes. 

_**Note:** This tutorial assumes that you have already completed the **Local-Show-Tive** getting started process. If you have not, complete the steps described in [Getting started](../getting-started.md), then return to this tutorial._

## Search for concerts by venue with cURL commands

1. In your preferred command line tool, start **Local-Show-Tive** locally by entering the following command:

    ```shell
    cd <your-github-workspace>/local-show-tive/api
    json-server -w local-show-tive-source.json
    ```
    You must keep this window open for the remainder of the process.

2. In a separate window of your command line tool, enter in the following GET command to retrieve a list of **Local-Show-Tive**'s venues.

    ```shell
    curl {base_url}/venues
    ```
    _**Note:** When run locally for testing, the `{base_url}` is generally `http://localhost:3000`._

    The response message lists every venue in **Local-Show-Tive**.

3. Identify the venue that you want to search concerts for by recording the venue's `id`. You will need the `id` for step 4.

   For this example, we will search for **The Depot**, which has an `id` of `1`.

4. Type in the following GET command to search for concerts at **The Depot**:

    ```shell
    curl {base_url}/concerts?venue_id=1
    ```
    _**Note:** When run locally for testing, the `{base_url}` is generally `http://localhost:3000`._

   You can change the `venue_id` value as you see fit. For more information, see the [Get concerts by venue id reference](../references/get-concerts-by-venue-id.md).

5.  Run the command.

    The command line tool returns a message listing all the concerts that are taking place at the specified venue (in this case, **The Depot**):

    ```js
    [
        {
            "venue_id": 2,
            "artist": "Tank & The Bangas",
            "date": "2025-01-18",
            "time": "8:00PM MST",
            "ticket price": "$32",
            "id": 1
        },
        {
            "venue_id": 2,
            "artist": "Periphery",
            "date": "2025-02-21",
            "time": "9:00PM MST",
            "ticket price": "$35",
            "id": 6
        }
    ]
    ```

## Search for concerts by venue in Postman

1. In your preferred command line tool, start **Local-Show-Tive** locally by entering the following command:

    ```shell
    cd <your-github-workspace>/local-show-tive/api
    json-server -w local-show-tive-source.json
    ```
    You must keep this window open for the remainder of the process.

2. Open the Postman app.

3. Create the following GET Request; you will use it to retrieve a list of **Local-Show-Tive**'s venues.

    ```shell
    GET {base_url}/venues
    ```
    _**Note:** When run locally for testing, the `{base_url}` is generally `http://localhost:3000`._

4. Click **Send**.

   The response message lists every venue in **Local-Show-Tive**.

5. Identify the venue that you want to search concerts for by recording the venue's `id`. You will need the `id` for step 6.

   For this example, we will search for **The Depot**, which has an `id` of `1`.

6. Create the following GET command to search for concerts at **The Depot**:

    ```shell
    POST {base_url}?venue_id=1
    ```
    _**Note:** When run locally for testing, the `{base_url}` is generally `http://localhost:3000`._

7. Click **Send**. 

   Postman returns a `200 OK` message and lists all the concerts that are taking place at the specified venue (in this case, **The Depot**):

   ```js
    [
        {
            "venue_id": 1,
            "artist": "JJ Grey & Mofro",
            "date": "2025-01-29",
            "time": "7:00PM MST",
            "ticket price": "N/A",
            "id": 2
        },
        {
            "venue_id": 1,
            "artist": "They Might Be Giants",
            "date": "2025-06-10",
            "time": "7:00PM MST",
            "ticket price": "$55",
            "id": 4
        }
    ]
   ```

## Related tutorials

For more concert tutorials, see the following topics:
- [Add a concert](add-a-concert.md)
- [Update a concert](update-a-concert.md)
- [Search for concerts by artist](search-for-concerts-by-artist.md)
- [Delete a concert](delete-a-concert.md)