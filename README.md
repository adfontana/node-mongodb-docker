# Node.JS/ MongoDB/ Docker

## Overview

REST API using NodeJS, MongoDB and Docker to create a containerized application. 

This app was created following all the steps in [Docker docs](https://docs.docker.com/language/nodejs/).

## Usage
Start the application
````
docker-compose -f docker-compose.dev.yml up --build
````
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