---
title: Getting Started
nav_order: 2
has_toc: false
---

# Getting Started

This document explains the prerequisite steps you need to take to being using **Local-Show-Tive**, and how to perform a test command on your development system.

This getting started process should take about 20 minutes.

## Prerequisite setup
To begin using **Local-Show-Tive**, you need to a [GitHub account](https://github.com) and a development system (Windows, Mac, or Linux) running a current or long-term support version.

You must also install the following packages on your machine. We recommend opening the links in separate brower tabs before you start installing the software.

* [Git](https://docs.github.com/en/get-started/quickstart/set-up-git) (this includes Git Bash, which we recommend using for running **Local-Show-Tive** commands)
* A fork of the [Local-Show-Tive repo](https://github.com/levigbeverly/local-show-tive)
* A current/LTS version of `node.js`
* A current version of [json-server](https://www.npmjs.com/package/json-server)
* A current copy of the database file. You can get this by syncing your fork of the **Local-Show-Tive** repo.
    * _**Tip**: If you're using a fork of the repo, create a working branch in which to do your tutorials. Create a new branch for each tutorial to prevent a mistake in one from affecting your work in another._
* The [Postman desktop app](https://www.postman.com/downloads/). You cannot use the web version because you will be running **Local-Show-Tive** on your development system with an `http://localhost` hostname.

## Test your development system

To test your development system:

1. Create and checkout a test branch of your fork of the loca-show-tive repo. Your `GitHub repo workspace` is the directory that contains your fork of the `local-show-tive` repo.

    ```shell
    cd <your GitHub repo workspace>
    ls
    # (see the local-show-tive directory in the list)
    cd local-show-tive
    git checkout -b tutorial-test
    cd api
    json-server -w local-show-tive-source.json
    ```

    If your development system is installed correctly, you should see
    the service start and show the service URL: `http://localhost:3000`.

2. Make a test call to the service.

    ```shell
    curl http://localhost:3000/concerts
    ```

3. If the service is running correctly, you should see a list of concerts from **Local-Show-Tive**, such as in this example:

    ```js
    [
        {
            "venue_id": "2",
            "artist": "Tank & The Bangas",
            "date": "2025-02-01",
            "time": "7:00PM MST",
            "ticket price": "$40",
            "id": 1
        },
        {
            "venue_id": 1,
            "artist": "JJ Grey & Mofro",
            "date": "2025-01-29",
            "time": "7:00PM MST",
            "ticket price": "N/A",
            "id": 2
        },
        ...
    ```

If you don't see the list of concerts, or receive an error in any step of the procedure, investigate and correct the error before continuing. Some common situations that cause errors include:

- You mistyped a command.
- You aren't in the correct directory.
- A required software component didn't install correctly.
- A required software component isn't up to date.

If you see the list of concerts from the service, you are ready to use **Local-Show-Tive**. We recommending viewing the [Quickstart](quickstart.md) to quickly set up your first venues and concert listings, or your can return the documentation [landing page](index.md) to view the **Local-Show-Tive** tutorials and references.
