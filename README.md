# waymaker-umbrella
An umbrella to hold all other projects into one single runnable artifact.  
- waymaker-frontend (web interface)
- waymaker-backend (api backend)
- waymaker-caddy (proxy server)


### Project initiation
To work with with this project, 
1. clone this repo
2. set environment variables into .env file
    ```
    cd waymaker-umbrella 
    touch .env
    ```
    - PROXY=
    - FRONTEND_WEB=
    - BACKEND_API=
    - BACKEND_WATSAPP=
    - DB_VERSION=
    - DB_HOST=
    - DB_PORT=
    - DB_USERNAME=
    - DB_PASSWORD=
    - DB_DBNAME=
3. turn on batch scripts in folder `auto` 
    ```
    chmod +x auto/init
    chmod +x auto/build
    ```
4. clone other projects in by running `auto/init`
5. build project for target environment `auto/build dev`
6. available environments as below:
    - dev (development)
    - prod (production)

### Additional project inclusion into `waymaker-umberlla`
#### New Folder
1. create folder, example: `waymaker-watsapp` outside of `waymaker-umbrella`
2. git init `waymaker-watsapp`

#### Umbrella Folder
1. .gitignore `waymaker-watsapp`
1. Add entry into .env, auto/init and auto/build
2. Adjust docker-compose.dev, docker-compose.prod 