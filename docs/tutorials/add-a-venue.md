---
layout: page
---

# Tutorial: Add a venue 

Use the following steps to quickly add a new venue in **Local-Show-Tive**. You can perform these steps using [cURL commands](#delete-a-venue-with-curl-commands) or in the [Postman application](#delete-a-venue-in-postman).

You will have to use a command-line tool to complete the tutorial. If you are a first-time user, we recommend using Git Bash. If you use a different command-line tool, you may need to adapt the provided syntax for your tool of choice.

The tutorial will take about five minutes. 

_**Note:** This tutorial assumes that you have already completed the **Local-Show-Tive** getting started process. If you have not, complete the steps described in [Getting started](../getting-started.md), then return to this tutorial._

## Add a venue with cURL commands

1. In your preferred command line tool, start **Local-Show-Tive** locally by entering the following command:

    ```shell
    cd <your-github-workspace>/local-show-tive/api
    json-server -w local-show-tive-source.json
    ```
    You must keep this window open for the remainder of the process.

2. In a separate window of your command line tool, enter the following POST command to create the new venue:

    ```shell
    curl POST {base_url}/venues
    ```
    _**Note:** When run locally for testing, the `{base_url}` is generally `http://localhost:3000`._

3.  [WIP, add details about the request body and running the command]

    The command line tool returns a message indicating that you successfully created the venue.

4. To validate that the new venue was successfully added, run the following GET command:

    ```shell
    curl {base_url}/venues
    ```
   The new venue appears in the response body.

## Add a venue in Postman

1. In your preferred command line tool, start **Local-Show-Tive** locally by entering the following command:

    ```shell
    cd <your-github-workspace>/local-show-tive/api
    json-server -w local-show-tive-source.json
    ```
    You must keep this window open for the remainder of the process.

2. Open the Postman app.

3. Create the following POST request; you will use it to create the new venue:

    ```shell
    POST {base_url}/venues
    ```
    _**Note:** When run locally for testing, the `{base_url}` is generally `http://localhost:3000`._

4. [WIP, add details about the request body and running the command]

5. Click **Send**. 

   Postman returns a `200 OK` message.

6. If you want to validate that the new venue was succesfully added, run the following GET request in Postman:

   ```shell
    {base_url}/venues
    ```
   The new venue appears in the response body.

## Related tutorials

[WIP]
