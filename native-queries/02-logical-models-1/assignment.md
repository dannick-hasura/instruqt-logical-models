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
Make sure Hasura is running
 =====

Now that we have the Hasura API available from the previous step let's make sure it is running.
```bash,run
cd cli-demo
```
Start the containers:
```bash,run
docker-compose up -d
```
Run the Hasura console and open the "Hasura Console" tab:
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

Step 1 - Add our logical model
=========

The logical model is used to define the response types for our data masking query. Let's define these output types first, then we will define the actual function to mask the data.
In the Hasura Console, if you are not already on the Logical Models tab then please head over to
[button label="Hasura Tab"](tab-1)
Data tab --> Native Queries --> Logical Models


🏁 Finish
=========

## Check

To complete this track, press **Check**
