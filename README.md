# wp_dev

## Prerequisites
Install Docker and Docker Compose

## Setup
You first need to run the database container to let it initialize
```
docker-compose up cdc_wp_db
```
Once this is complete (give it a few minutes and watch the terminal) you can stop the db container via Ctrl-C
Next start up all services via
```
docker-compose up -d
```
Once all services are up you need to log into WordPress to complete the install.  To do this open a browser and connect to http://localhost:8080.  Complete the short setup wizard and WordPress should be installed.

We have mounted two volumes for development, one for themes, the other for plugins.  They are:
./wp-content/themes
./wp-content/plugins
You will want to change permissions for these directories locally by running:
```
sudo chmod -R 777 wp-content
```

### Run
To start dev environment:
```
docker-compose up -d
```
To stop dev environment:
```
docker-compose stop
```
### Notes
WordPress URL: http://localhost:8080
phpmyadmin URL: http://localhost:8181
WordPress database name: cdc_wordpress

There is a volume for uploads, but its contents should be ignored by git and not checked into version control.
