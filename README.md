# PegaInDocker

1. Introduction
2. Architecture
3. Steps to install Pega in Docker
    a. Start docker
    b. Find docker image sources used in this project
    c. Download postgres JDBC driver
    d. Download Pega.dump file
    e. create Dockerfile
    f. Build docker image
    g. Run Postgres in Docker
    h. Dump pega.dump inside postgres container
    i. Join a Postgres container in a Docker network
    j. Run Pega in Docker
    k. Join Pega container in docker network
    l. Access Pega from local machine

    Important CMDs:
    # list all containers
        docker ps -a
    # Kill the docker container
        docker kill pegapgsql
    # Kill & Remove together
        docker kill pegapgsql | docker rm pegapgsql
    # Remove the container
        docker rm pegapgsql
    # build the postgres image:
        docker build -t pegapostgres:latest .
    # Run the postgres container:
        docker run --name pegapgsql -p 5432:5432 pegapostgres:latest
    # Build Pega image
        docker build -t pega:latest .
    # Run Pega
        docker run --name pega -p 8080:8080 pega:latest
    # Pega access url
    http://localhost:8080/