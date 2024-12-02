---
title: Quickstart
nav_order: 3
has_toc: false
---
# Quickstart

If you have just set up the **Local-Show-Tive** service on your machine, complete the follow steps to add your first venues and concert listings. To get started, we recommend creating three venues and three concert listings, but you can use the following process to create as many as you like.

This process will take about 15 minutes.

You will have to use a command-line tool to complete the quickstart steps. We recommend using Git Bash. If you use a different command-line tool, you may need to adapt the provided syntax for your tool of choice.

_**Note:** These steps assume that you have already completed the **Local-Show-Tive** getting started process. If you have not, complete the steps described in [Getting started](getting-started.md), then return to this topic._

## Add your first venues and concert listings

1. In your preferred command line tool, start **Local-Show-Tive** locally by entering the following command:

    ```shell
    cd <your-github-workspace>/local-show-tive/api
    json-server -w local-show-tive-source.json
    ```
    You must keep this window open for the remainder of the process.

2. In a separate window of your command line tool, type in the following POST command to create your first venue:

    ```shell
    curl -X POST {base_url}/venues -H "Content-Type: application/json" -d '{"name": "Baltimore Soundstage", "city": "Baltimore, MD", "venue type": "indoor", "age restriction": "21+"}'
    ```
    _**Note:** When run locally for testing, the `{base_url}` is generally `http://localhost:3000`._

   For more information about this command, see the [Add venue reference](references/post-add-venue.md).

3. Run the command.

   The command line tool returns a message indicating that you successfully created the venue. The return message lists the new venue, the request body values you specified, and an automatically assigned `id` value. 
   
   Congratulations, you've added your first venue!

4. Repeat steps 2 and 3 twice to add two more venues (or as many venues as you like). For each new venue, update the `-d` response body values to whatever you see fit. Ensure that you follow the same formatting as the example command and that your `-d` values are valid based on the following rules:

    | Property name | Type | Description |
    | ------------- | ----------- | ----------- |
    | `name` | string | Enter the name of the venue. |
    | `city` | string | Enter the city and state (abbreviated) the venue is located in (for example, `Baltimore, MD `). |
    | `type` | string | Indicate whether the venue is indoor or outdoor. The valid options are `indoor` and `outdoor`. |
    | `age restriction` | string | Indicate whether the venue has an age restriction. The valid options are `all ages` and `21+`.  | 

5. To validate that the new venues were successfully added, run the following GET command:

    ```shell
    curl {base_url}/venues
    ```
   The new venues appear in the response body.

6. Type in the following POST command to create your first new concert listing:

    ```shell
    curl -X POST {base_url}/concerts -H "Content-Type: application/json" -d '{"venue_id": 1, "artist": "Switchfoot", "date": "2025-07-06", "time": "8:00PM EST", "ticket price": "$40"}'
    ```
    _**Note:** When run locally for testing, the `{base_url}` is generally `http://localhost:3000`._

   For more information about this command, see the [Add concert reference](references/post-add-concert.md).

7.  Run the command.

    The command line tool returns a message indicating that you successfully created the concert. The return message lists the new concert, the request body values you specified, and an automatically assigned `id` value. 
    
    Congratulations, you've added your first concert listing!

8. Repeat steps 6 and 7 twice to add two more concert listings (or as many concert listings as you like). For each new concert, update the `-d` response body values to whatever you see fit (keep in mind that the `venue_id` equates to the `id` shown in the step 5 response message). Ensure that you follow the same formatting as the example command and that your `-d` values are valid based on the following rules:

    | Property name | Type | Description |
    | ------------- | ----------- | ----------- |
    | `venue_id` | integer | Enter the `venue_id` of the venue the concert is taking place at. |
    | `artist` | string | Enter the name of the artist performing at the concert. |
    | `date` | string | Enter the date the concert takes place on in `YYYY-MM-DD` format. |
    | `time` | string | Enter the time the concert takes place at in the following format: {time}{AM/PM} {abbreviated time zone} (for example, `8:00PM MST`).|
    | `ticket price` | string | Enter the concert ticket price in the following format: {currency type}{amount} (for example, `$26`).|

9. To validate that the new concerts were successfully added, run the following GET command:

    ```shell
    curl {base_url}/concerts
    ```
   The new concerts appear in the response body.

Now that you have added your first venues and concerts, return the documentation [landing page](index.md) to view the **Local-Show-Tive** tutorials and references.
