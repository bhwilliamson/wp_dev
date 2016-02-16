# wp_dev
## Prerequisites
Install Docker and Docker Compose
## Setup
You first need to run the database container to let it initialize
```
docker-compose up cdc_wp_db
```
Once this is complete (give it a few minutes and watch the terminal) you can stop the db container via Ctrl-C
### Run
To start dev environment:
```
docker-compose up -d
```
To stop dev environment:
```
docker-compose stop
```

