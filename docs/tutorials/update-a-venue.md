---
layout: page
---

# Tutorial: Update a venue

Use the following steps to change an existing venue listing's details in **Local-Show-Tive**. You can perform these steps using [cURL commands](#update-a-venue-with-curl-commands) or in the [Postman application](#update-a-venue-in-postman).

You will have to use a command-line tool to complete the tutorial. If you are a first-time user, we recommend using Git Bash. If you use a different command-line tool, you may need to adapt the provided syntax for your tool of choice.

The tutorial will take about five minutes. 

_**Note:** This tutorial assumes that you have already completed the **Local-Show-Tive** getting started process. If you have not, complete the steps described in [Getting started](../getting-started.md), then return to this tutorial._

## Update a venue with cURL commands

1. In your preferred command line tool, start **Local-Show-Tive** locally by entering the following command:

    ```shell
    cd <your-github-workspace>/local-show-tive/api
    json-server -w local-show-tive-source.json
    ```
    You must keep this window open for the remainder of the process.

2. In a separate window of your command line tool, enter the following GET command to retrieve a complete list of venues:

    ```shell
    curl {base_url}/venues
    ```
    _**Note:** When run locally for testing, the `{base_url}` is generally `http://localhost:3000`._

    The command line tool returns a complete list of venues stored in **Local-Show-Tive**.

3. Identify which venue you would like to update. Keep in mind what the venue's `id` is; you will need it to run the update command. 

    For this example, we will edit a venue that has an `id` of `1`.

4. Enter the following PUT command. 

    ```shell
    curl -X PUT {base_url}/venues/1 -H "Content-Type: application/json" -d '{"name": "The Depot", "city": "South Salt Lake, UT", "venue type": "indoor", "age restriction": "21+"}'
    ```
    _**Note:** When run locally for testing, the `{base_url}` is generally `http://localhost:3000`._

    In this example, we will update the venue with a new name (`The Depot`), city (`South Salt Lake, UT`), venue type (`indoor`), and age restriction (`21+`). However, you can change the venue `id` and any of the `-d` response body values as you see fit. You must include all venues properties in the command body, even if you are not updating some of the properties. If you run the update command without some of the properties, those properties are erased from the venue and will need to be re-added in another update command. For more information, see the [Add venue reference](../references/post-add-venue.md).

    The command line tool returns a message showing the newly-updated venue object.

## Update a venue in Postman

1. In your preferred command line tool, start **Local-Show-Tive** locally by entering the following command:

    ```shell
    cd <your-github-workspace>/local-show-tive/api
    json-server -w local-show-tive-source.json
    ```
    You must keep this window open for the remainder of the process.

2. Open the Postman app.

3. Create the following GET request; you will use it to retrieve a complete list of venues:

    ```shell
    GET {base_url}/venues
    ```
    _**Note:** When run locally for testing, the `{base_url}` is generally `http://localhost:3000`._

4. Click **Send**. 

   Postman returns a `200 OK` message, and the response body lists all venues in the **Local-Show-Tive** database.

5. Identify which venue you would like to delete. Keep in mind what the venue's `id` is; you will need it to run the deletion command.

    For this example, we will edit a venue that has an `id` of `1`.

6. Create the following PUT request. 

    ```shell
    PUT {base_url}/venues/1
    ```
    _**Note:** When run locally for testing, the `{base_url}` is generally `http://localhost:3000`._

7. Click the **Body** tab.

8. In the **Body** menu, select the **raw** radio button.

9. In the space below the **raw** radio button, enter the following response body values:

   ```js
   {
    "name": "The Depot",
    "city": "South Salt Lake, UT",
    "venue type": "indoor",
    "age restriction": "21+"
   }
   ```
    In this example, we will update the venue with a new name (`The Depot`), city (`South Salt Lake, UT`), venue type (`indoor`), and age restriction (`21+`). However, you can change the venue `id` and any of the `-d` response body values as you see fit. You must include all venues properties in the command body, even if you are not updating some of the properties. If you run the update command without some of the properties, those properties are erased from the venue and will need to be re-added in another update command. For more information, see the [Add venue reference](../references/post-add-venue.md).

10. Click **Send**. 

   Postman returns a `200 OK` message and shows the newly-updated venue object.

## Related tutorials

For more venue tutorials, see the following topics:
- [Add a venue](update-a-venue.md)
- [Delete a venue](delete-a-venue.md)