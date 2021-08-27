# Node.JS/ MongoDB/ Docker

## Overview

REST API using NodeJS, MongoDB and Docker to create a containerized application. 

This app was created following all the steps in [Docker docs](https://docs.docker.com/language/nodejs/).

## Prerequisites
- [Node.js](https://nodejs.org/en/)
- [Docker](https://docs.docker.com/engine/install/)

## Install
    npm install

## Usage
Start the application with [Docker Compose](https://docs.docker.com/compose/), run: 
````
docker-compose -f docker-compose.dev.yml up --build
````
This will install and build the images, besides start the containers.

Check if the application is connected to the database and is able to add a note.
```
 curl --request POST \
  --url http://localhost:8000/notes \
  --header 'content-type: application/json' \
  --data '{
    "name": "this is a note",
    "text": "this is a note that I wanted to take while I was working on writing a blog post.",
    "owner": "peter"
    }'
```

## Debug
The `launch.json` file was set to debug a containerized app in VSCode. 

After start the app, you will be able to add some breakpoints and debug the source code when needed.
