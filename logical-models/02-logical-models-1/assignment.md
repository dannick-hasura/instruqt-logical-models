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
  workdir: instruqt-logical-models/hasura/
- title: Hasura Console
  type: service
  hostname: docker-vm
  path: /console/data/native-queries/logical-models
  port: 8080
difficulty: ""
timelimit: 600
---
# Logical Models
Logical Models are a GraphQL representation of database data. They provide an abstraction over the underlying database in a simlar way to using a View on your database. The logic model will define the data types that you will be working with in this data masking function.
```bash,run
docker-compose up -d && hasura metadata apply
```

Step 1 - Add our logical model
=========
Let's begin by defining the data types. Head over to the Hasura console.

Data tab --> Native Queries --> Logical Models.
![Logical Models Tab](../assets/Screenshot%202024-01-31%20at%206.43.54%E2%80%AFPM.png)

Add a new logical model, selecting the demo clinic database as the source. Let's name this model `patient_masked_data`.
![Screenshot 2024-02-01 at 4.19.56 PM.png](../assets/Screenshot%202024-02-01%20at%204.19.56%E2%80%AFPM.png)

Now we will define the data types we plan to return from our data masking function that we haven't yet created. This will help us think about the data model before we build the functionality. Add the fields as follows and create the model.
![Screenshot 2024-02-01 at 4.20.21 PM.png](../assets/Screenshot%202024-02-01%20at%204.20.21%E2%80%AFPM.png)

Step 2 - Create our data masking function
=========

# Native Queries
Now we get to the fun part, native queries allow us to leverage the underlying functionality of the database language -- in this case Postgres SQL. Let's write a SQL function that will return patient data but mask several pieces of private information.



🏁 Finish
=========

## Check

To complete this track, press **Check**
