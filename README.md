# bal-wordpress-docker
bits &amp; likes local docker compose development setup

## Setup
This is a basic docker development setup for WordPress. It contains of a `docker-compose.yml` file that creates containers for WordPress, MySQL and adminer. 
Additionally there is a php folder that has a `custom.ini` file, which can be used to add or extend the default php.ini configuration. 
The WordPress service inside of the `docker-compose.yml` file also has two pre mounted folders: `themes` and `plugins`. They are mounted to the default WordPress themes and plugins folders, so that you can add your custom plugins or themes. Also the `docker-compose.yml` file has some comments, so that you can easily change that behaviour. 

## How to use
You can fork the repository for your own project as part of the development process. After cloning your repository, move into that folder and start the containers with `docker compose up -d`. 
It will start the WordPress, MySQL and adminer containers. The default database login is `root` with the password `root` and a default database called `db`. 
When browsing to `http://localhost` you should get to the default WordPress installation process. `http://localhost:8080` can be used for adminer. 

## Commands
- docker-compose down -v --remove-orphans --rmi all