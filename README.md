# Next.js OpenJira App

## Prerequisites.
```
mongoose: "^6.2.0"
Docker
node": "17.0.14"

```

## Add this file in root directory.

docker-compose.yaml:
```
services:
  entriesdb:
    image: mongo:(version that you install locally in your computer)
    container_name: entries-database
    ports:
      - 27017:27017
    volumes:
      - ./mongo:/data/db
```


To run locally, you need the database.
```
docker-compose up -d
```

* The -d, stands for __detached__.


## Set the environment variables
Rename the __.env.template__ file to __.env__.
* MongoDB Local URL:
```
MONGO_URL=mongodb://localhost:27017/entriesdb
```

* Rebuild node modules and start Next
```
yarn install
yarn dev
```


## Fill the database with test information.

Will call:
```
http://localhost:3000/api/seed
```


## More information.


Click [mongo](https://www.mongodb.com/) to go to Mongo docs. 
Click [docker](https://www.docker.com/) to go to docker documentation.









