---
slug: running-hasura-in-docker
id: yg1urnnqufn4
type: challenge
title: Running Hasura
teaser: Learn how to build and run the Hasura container
notes:
- type: text
  contents: |+
    # Logical Models

    Logical Models are a GraphQL representation of database data. They provide an abstraction over the underlying database. Logical Models are a new approach from Hasura and are currently used by the Native Queries and the GraphQL API for a native database query.

    In this first challenge we will set up the course environment by running Hasura in a docker container and connecting to our demo database.

    # What is Hasura
    Hasura automates the creation of your data APIs. Just point Hasura to your data and watch as it instantly generates a robust GraphQL API with CRUD operations!

tabs:
- title: Terminal
  type: terminal
  hostname: docker-vm
- title: Hasura
  type: service
  hostname: docker-vm
  path: /console/data/
  port: 8080
- title: VS Code
  type: service
  hostname: docker-vm
  path: /
  port: 8090
difficulty: ""
timelimit: 600
---

🧪 Init the local project
=======================

Let's create a new project locally called `cli-demo`:

```bash,run
hasura init cli-demo
```

This will create a new directory called `cli-demo` with the following structure:

```nocopy
cli-demo
├── config.yaml
├── migrations
├── metadata
├── seeds
```

Change into that directory:

```bash,run
cd cli-demo
```

> [!IMPORTANT]
> **WHAT IF I ALREADY HAVE A PROJECT?**
>
>If you followed our Quickstart with Docker, you'll already have a local project. In that case, in the project's directory, you can run the following command to initialize the current directory as a Hasura project:
>```run
>hasura init .

🏃 Start the containers
===

This docker-compose.yaml file contains the configuration for the Hasura GraphQL Engine and a Postgres database:

```bash,run
curl https://raw.githubusercontent.com/hasura/graphql-engine/master/install-manifests/docker-compose/docker-compose.yaml > docker-compose.yaml
```

Now, start the containers:

```bash,run
docker-compose up -d
```
🏃 Run the Hasura Console
===

Hasura can be interacted with using the Console (user interface) or through code. We will interact with Hasura using the Hasura Console, run the console using the CLI:
```bash,run
hasura console --address 0.0.0.0 --no-browser
```
> [!NOTE]
> ```hasura console``` opens the console
>
> ``` --address 0.0.0.0``` (optional) to specify a host.The default is http://localhost:9695
>
> ```--no-browser``` (optional) prevents Instruqt from trying to open a separate browser tab.
> We will instead just head over to the existing "Hasura Console" tab.