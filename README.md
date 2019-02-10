## About
This project should help front-end developers quickly start local development using Docker and allow deploys to servers easier.
The creation of this project was inspired by [Laradock](https://github.com/laradock/laradock), [nginx-proxy](https://github.com/jwilder/nginx-proxy) and [this article](https://medium.com/@pentacent/nginx-and-lets-encrypt-with-docker-in-less-than-5-minutes-b4b8a60d3a71)

## Installation
- Enter into your project and run
    ```
    git clone https://github.com/maxwell-hub/frontdock.git docker
    ```
- Enter into `./docker/` (folder with docker-compose.yml)
- Remove git files to avoid conflict of git roots
    ```
    rm -rf .git
    ```
- Clone .env file and configure environment variables
    ```
    cp env-example .env && cp ./nginx/sites/app.conf.example ./nginx/sites/app.conf
    ```
- Run containers
    ```
    docker-compose up -d
    ```

## Using
- After running, check web server on availability `http://localhost`
- Enter into `node` container through your IDE or using a command
    ```
    docker exec -it docker_node_1 bash
    ```
- Check that all successful installed
    ```
    node --version && npm -v && yarn --version
    ```

