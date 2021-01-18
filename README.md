# Project: openapi-mock-open-banking

## About this
This project allows users to run Open Banking using Docker based on local machines or using [PWD - Play with Docker](https://labs.play-with-docker.com/). PWD is a Docker playground which allows users to run Docker commands in a matter of seconds.


## Dependencies
* [OpenAPI Mock Server](https://github.com/muonsoft/openapi-mock)
* [Docker](https://www.docker.com/)
* [PWD - Play With Docker](https://labs.play-with-docker.com/) (It's alternative to expose the mock through internet running in the cloud).


## Getting started to run on local machine
1. Download and install [Docker](https://www.docker.com/).

2. Downloads an image of [OpenAPI Mock Server](https://github.com/muonsoft/openapi-mock)

```bash
docker pull muonsoft/openapi-mock
```

3. Fork this repository on Github.

4. Clone your forked repository (not our original one) to your hard drive with git clone https://github.com/YOURUSERNAME/openapi-mock-open-banking.git

5. Access directory openapi-mock-open-banking. 
```bash
cd openapi-mock-open-banking
```

6. Run the image of openapi-mock-open-banking
```bash
docker-compose up
```

Alternatively it's possible to run as a docker command:

```
bash
docker run -p 8080:8080 -e "OPENAPI_MOCK_SPECIFICATION_URL=https://raw.githubusercontent.com/luankevinferreira/areadesenvolvedor-widdershins/master/documentation/source/swagger/swagger_open_banking_apis.yaml" -e "OPENAPI_MOCK_USE_EXAMPLES=if_present" --rm muonsoft/openapi-mock
```


## Getting started to run in the cloud
1. Access [PWD](https://labs.play-with-docker.com/) and start a new session with your [Docker Hub](https://hub.docker.com/) credentials.

2. Once your session is active click on "Add New Instance".

3. A new instance will start with a Docker Engine ready to accept commands.

4. Downloads an image of [OpenAPI Mock Server](https://github.com/muonsoft/openapi-mock)

```bash
docker pull muonsoft/openapi-mock
```

5. Fork this repository on Github.

6. Clone your forked repository (not our original one) to your hard drive with git clone https://github.com/YOURUSERNAME/openapi-mock-open-banking.git

7. Access directory openapi-mock-open-banking. 
```bash
cd openapi-mock-open-banking
```

8. Run the image of openapi-mock-open-banking
```bash
docker-compose up
```

Alternatively it's possible to run as a docker command:

```
bash
docker run -p 8080:8080 -e "OPENAPI_MOCK_SPECIFICATION_URL=https://raw.githubusercontent.com/luankevinferreira/areadesenvolvedor-widdershins/master/documentation/source/swagger/swagger_open_banking_apis.yaml" -e "OPENAPI_MOCK_USE_EXAMPLES=if_present" --rm muonsoft/openapi-mock
```

9. At the end of the process you should see the message such as "Creating openapi_mock ... done". The option -p 8080:8080 exposes the container port 8080 as the host port 8080 to the world.


10. As a result a port 8080 link should have become active next to the IP. Click on it to access your openapi-mock-open-banking service or use this curl command:
curl 'http://<YOUR_ID_PWD>.direct.labs.play-with-docker.com/open-banking/discovery/v1/status'

Alternatively it's possible to run this command to test that the server successfully run:

```
bash
curl 'http://localhost:8080/v1/pets'
```

## REFERENCES
- [OpenAPI Mock Server](https://github.com/muonsoft/openapi-mock)
- [Docker](https://www.docker.com/)
- [PWD - Play With Docker](https://labs.play-with-docker.com/)