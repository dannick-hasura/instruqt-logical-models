---
slug: logical-models-1
id: n52iczz9fmtw
type: challenge
title: Creating a Logical Model
teaser: We will use a logical model and native query to create a simple query that
  masks data at the database level.
notes:
- type: text
  contents: |-
    # Logical Models and Native Queries

    Logical Models are a GraphQL representation of database data. They provide an abstraction over the underlying database.

    Logical Models are a new approach from Hasura and are currently used by the Native Queries feature to automatically create a GraphQL API for a native database query.
tabs:
- title: Terminal
  type: terminal
  hostname: docker-vm
  workdir: $HOME/cli-demo
- title: Hasura Console
  type: service
  hostname: docker-vm
  path: /console/data
  port: 8080
difficulty: ""
timelimit: 600
---
# Logical Models
Logical Models are a GraphQL representation of database data. They provide an abstraction over the underlying database in a simlar way to using a View on your database. The logic model will define the data types that you will be working with in this data masking function.

Step 1 - Add our logical model
=========
Let's begin by defining the data types. Head over to the Hasura console.

Data tab --> Native Queries --> Logical Models.
![Logical Models Tab](../assets/Screenshot%202024-01-31%20at%206.43.54%E2%80%AFPM.png)

Add a new logical model

Step 2 - Create our data masking function
=========


🏁 Finish
=========

## Check

To complete this track, press **Check**
