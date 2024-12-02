---
parent: Tutorials
nav_order: 4
---

# Tutorial: Add a concert 

Use the following steps to quickly add a new concert in **Local-Show-Tive**. You can perform these steps using [cURL commands](#add-a-concert-with-curl-commands) or in the [Postman application](#add-a-concert-in-postman).

You will have to use a command-line tool to complete the tutorial. If you are a first-time user, we recommend using Git Bash. If you use a different command-line tool, you may need to adapt the provided syntax for your tool of choice.

The tutorial will take about five minutes. 

_**Note:** This tutorial assumes that you have already completed the **Local-Show-Tive** getting started process. If you have not, complete the steps described in [Getting started](../getting-started.md), then return to this tutorial._

## Add a concert with cURL commands

1. In your preferred command line tool, start **Local-Show-Tive** locally by entering the following command:

    ```shell
    cd <your-github-workspace>/local-show-tive/api
    json-server -w local-show-tive-source.json
    ```
    You must keep this window open for the remainder of the process.

2. In a separate window of your command line tool, type in the following POST command to create the new concert:

    ```shell
    curl -X POST {base_url}/concerts -H "Content-Type: application/json" -d '{"venue_id": 1, "artist": "Switchfoot", "date": "2025-07-06", "time": "8:00PM MST", "ticket price": "$40"}'
    ```
    _**Note:** When run locally for testing, the `{base_url}` is generally `http://localhost:3000`._

   You can change any of the `-d` response body values as you see fit. For more information, see the [Add concert reference](../references/post-add-concert.md).

4.  Run the command.

    The command line tool returns a message indicating that you successfully created the concert. The return message lists the new concert, the request body values you specified, and an automatically assigned `id` value.

5. To validate that the new concert was successfully added, run the following GET command:

    ```shell
    curl {base_url}/concerts
    ```
   The new concert appears in the response body.

## Add a concert in Postman

1. In your preferred command line tool, start **Local-Show-Tive** locally by entering the following command:

    ```shell
    cd <your-github-workspace>/local-show-tive/api
    json-server -w local-show-tive-source.json
    ```
    You must keep this window open for the remainder of the process.

2. Open the Postman app.

3. Create the following POST request; you will use it to create the new concert:

    ```shell
    POST {base_url}/concerts
    ```
    _**Note:** When run locally for testing, the `{base_url}` is generally `http://localhost:3000`._

4. Click the **Body** tab.

5. In the **Body** menu, select the **raw** radio button.

6. In the space below the **raw** radio button, enter the following response body values:

   ```js
   {
   "venue_id": 1,
   "artist": "Switchfoot",
   "date": "2025-07-06",
   "time": "8:00PM MST",
   "ticket price": "$40"
   }
   ```
   You can change any of the response body values as you see fit. For more information, see the [Add concert reference](../references/post-add-concert.md).

8. Click **Send**. 

   Postman returns a `201 Created` message. The return message lists the new concert, the request body values you specified, and an automatically assigned `id` value.

9. If you want to validate that the new concert was succesfully added, run the following GET request in Postman:

   ```shell
    {base_url}/concerts
    ```
   The new concert appears in the response body.

   ## Related tutorials
   
   For more concert tutorials, see the following topics:
   - [Update a concert](update-a-concert.md)
   - [Search for concerts by artist](serach-for-concerts-by-artist.md)
   - [Search for concerts by venue](search-for-concerts-by-venue.md)
   - [Delete a concert](delete-a-concert.md)
