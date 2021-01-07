## How to run

`docker-compose up`

Alternatively it's possible to run as a docker command:

`docker run -p 8080:8080 -e "OPENAPI_MOCK_SPECIFICATION_URL=https://raw.githubusercontent.com/luankevinferreira/areadesenvolvedor-widdershins/master/documentation/source/swagger/swagger_open_banking_apis.yaml" -e "OPENAPI_MOCK_USE_EXAMPLES=if_present" --rm muonsoft/openapi-mock`

### Run in the cloud

It's possible to use [Docker Playground](https://labs.play-with-docker.com/) to run the command and expose the mock through internet.

## REFERENCES

- https://github.com/muonsoft/openapi-mock