---
parent: Tutorials
nav_order: 5
---

# Tutorial: Update a concert

Use the following steps to change an existing concert listing's details in **Local-Show-Tive**. You can perform these steps using [cURL commands](#update-a-concert-with-curl-commands) or in the [Postman application](#update-a-concert-in-postman).

You will have to use a command-line tool to complete the tutorial. If you are a first-time user, we recommend using Git Bash. If you use a different command-line tool, you may need to adapt the provided syntax for your tool of choice.

The tutorial will take about five minutes. 

_**Note:** This tutorial assumes that you have already completed the **Local-Show-Tive** getting started process. If you have not, complete the steps described in [Getting started](../getting-started.md), then return to this tutorial._

## Update a concert with cURL commands

1. In your preferred command line tool, start **Local-Show-Tive** locally by entering the following command:

    ```shell
    cd <your-github-workspace>/local-show-tive/api
    json-server -w local-show-tive-source.json
    ```
    You must keep this window open for the remainder of the process.

2. In a separate window of your command line tool, enter the following GET command to retrieve a complete list of concerts:

    ```shell
    curl {base_url}/concerts
    ```
    _**Note:** When run locally for testing, the `{base_url}` is generally `http://localhost:3000`._

    The command line tool returns a complete list of concerts stored in **Local-Show-Tive**.

3. Identify which concert you would like to update. Keep in mind what the concert's `id` is; you will need it to run the update command. 

    For this example, we will edit a concert that has an `id` of `1`.

4. Enter the following PUT command. 

    ```shell
    curl -X PUT {base_url}/concerts/1 -H "Content-Type: application/json" -d '{"venue_id": "2", "artist": "Tank & The Bangas", "date": "2025-02-01", "time": "7:00PM MST", "ticket price": "$40"}'
    ```
    _**Note:** When run locally for testing, the `{base_url}` is generally `http://localhost:3000`._

    In this example, we will update the concert with a new venue_id (`2`), artist (`Tank & The Bangas`), date (`2025-02-01`), time (`7:00PM MST`), and ticket price (`$40`). However, you can change the concert `id` and any of the `-d` response body values as you see fit. You must include all concerts properties in the command body, even if you are not updating some of the properties. If you run the update command without some of the properties, those properties are erased from the concert and will need to be re-added in another update command. For more information, see the [Add concert reference](../references/post-add-concert.md).

    The command line tool returns a message showing the newly-updated concert object.

## Update a concert in Postman

1. In your preferred command line tool, start **Local-Show-Tive** locally by entering the following command:

    ```shell
    cd <your-github-workspace>/local-show-tive/api
    json-server -w local-show-tive-source.json
    ```
    You must keep this window open for the remainder of the process.

2. Open the Postman app.

3. Create the following GET request; you will use it to retrieve a complete list of concerts:

    ```shell
    GET {base_url}/concerts
    ```
    _**Note:** When run locally for testing, the `{base_url}` is generally `http://localhost:3000`._

4. Click **Send**. 

   Postman returns a `200 OK` message, and the response body lists all concerts in the **Local-Show-Tive** database.

5. Identify which concert you would like to delete. Keep in mind what the concert's `id` is; you will need it to run the deletion command.

    For this example, we will edit a concert that has an `id` of `1`.

6. Create the following PUT request. 

    ```shell
    PUT {base_url}/concerts/1
    ```
    _**Note:** When run locally for testing, the `{base_url}` is generally `http://localhost:3000`._

7. Click the **Body** tab.

8. In the **Body** menu, select the **raw** radio button.

9. In the space below the **raw** radio button, enter the following response body values:

   ```js
   {
   "venue_id": 2,
   "artist": "Tank & The Bangas",
   "date": "2025-02-01",
   "time": "7:00PM MST",
   "ticket price": "$40"
   }
   ```
   In this example, we will update the concert with a new venue_id (`2`), artist (`Tank & The Bangas`), date (`2025-02-01`), time (`7:00PM MST`), and ticket price (`$40`). However, you can change the concert `id` and any of the `-d` response body values as you see fit. You must include all concerts properties in the command body, even if you are not updating some of the properties. If you run the update command without some of the properties, those properties are erased from the concert and will need to be re-added in another update command. For more information, see the [Add concert reference](../references/post-add-concert.md).

10. Click **Send**. 

   Postman returns a `200 OK` message and shows the newly-updated concert object.

## Related tutorials

For more concert tutorials, see the following topics:
- [Add a concert](add-a-concert.md)
- [Search for concerts by artist](serach-for-concerts-by-artist.md)
- [Search for concerts by venue](search-for-concerts-by-venue.md)
- [Delete a concert](delete-a-concert.md)
