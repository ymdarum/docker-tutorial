# Main
This is the repo created based on Docker tutorial. Below are my machine specs:

- OS : Windows 10
- Docker Info:
  - version : 3.1.0 (51484)
  - Engine  : 20.10.2
  - Docker-Compose : 1.27.4

### Pre-requisites
1. Install [Docker Desktop](https://www.docker.com/products/docker-desktop)
2. Install [Docker-Compose](https://docs.docker.com/compose/install/) - normally with Docker Desktop, this will be bundle together
    To check docker version:
      - `docker version`
      - `docker-compose version`
 
### Steps - all steps are done is Windows Subsystem for Linux CMD
1. Navigate into the intended git directory and run init command
    - `git init` 
2. Clone this repo by doing fork and clone the repo
    - `git clone https://github.com/ymdarum/docker-tutorial.git` - clone the git repo
3. Rename the docker-tutorial directory to app
    - `mv docker-tutorial app`
4. Change directory to /app
    - `cd app/`
5. Run the app with docker-compose using -d in detach mode (background)
    - `docker-compose up -d` 

6. Wait for a minute and open your browser to navigate to http://localhost:3000/

## Other commands
Other useful docker command:
  - `docker-compose logs` - Displays log output
  - `docker-compose ps` - List containers
  - `docker-compose down` - Stop containers in current directory
  - `docker network ls` - List all docker network
  - `docker volume ls` - List all docker volume
  - `docker volume create <volume-name>` - Create docker volume (to persist data)
  - `docker network create <network-name>` - Create network inside container

## Connect to database
If you want to use Ad hoc query, run below command:
- `docker exec -it <mysql-container-id> mysql -p` 
  - mysql-container-id can be found by running docker-compose ps 
  - mysql password = secret

## Credits
- [Docker 101](https://www.docker.com/101-tutorial)
- [docker-airflow-tutorial](https://github.com/tuanavu/airflow-tutorial)
- [git tutorial](https://www.atlassian.com/git/tutorials)
- [git delete branch](https://www.freecodecamp.org/news/how-to-delete-a-git-branch-both-locally-and-remotely/)
