---
parent: Tutorials
nav_order: 3
---

# Tutorial: Delete a venue 

Use the following steps to quickly identify and delete a venue in **Local-Show-Tive**. You can perform these steps using [cURL commands](#delete-a-venue-with-curl-commands) or in the [Postman application](#delete-a-venue-in-postman).

You will have to use a command-line tool to complete the tutorial. If you are a first-time user, we recommend using Git Bash. If you use a different command-line tool, you may need to adapt the provided syntax for your tool of choice.

The tutorial will take about five minutes. 

_**Note:** This tutorial assumes that you have already completed the **Local-Show-Tive** getting started process. If you have not, complete the steps described in [Getting started](../getting-started.md), then return to this tutorial._

## Delete a venue with cURL commands

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

3. Identify which venue you would like to delete. Keep in mind what the venue's `id` is; you will need it to run the deletion command. 

4. Enter the following DELETE command. Specify the venue you want to delete by replacing `{id}` with the venue's `id` at the end of the request.

    ```shell
    curl -X DELETE {base_url}/venues/{id}
    ```

    The command line tool returns a message indicating that you successfully deleted the venue.

    If you want to validate the deletion, re-run the GET command from step 2. The deleted venue does not appear in the response body.

## Delete a venue in Postman

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

6. Create the following DELETE request. Specify the venue you want to delete by replacing `{id}` with the venue's `id` at the end of the request.

    ```shell
    DELETE {base_url}/venues/{id}
    ```

7. Click **Send**. 

   Postman returns a `200 OK` message, indicating that you successfully deleted the venue.

   If you want to validate the deletion, re-run the GET request from step 3. The deleted venue does not appear in the response body.

## Related tutorials

For more tutorials about managing venues, see the following topics:
- [Add a venue](add-a-venue.md)
- [Update a venue](update-a-venue.md)
