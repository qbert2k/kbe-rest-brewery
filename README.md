# SFG Beer Works - RESTful Brewery Service

This project is to support learning about Restful APIs. 

You can access the API documentation [here](https://sfg-beer-works.github.io/brewery-api/#tag/Beer-Service) 

## Building a Docker Image

```shell
docker build -f ./src/main/dockerBase/Dockerfile -t kbe-rest .
```

## Building From layers

```shell
docker build -f ./src/main/docker/Dockerfile -t kbe-rest .
```

## Run Docker Image

```shell
docker run -p 8080:8080 -d kbe-rest
```

## Connect with Spring Framework Guru
* Spring Framework Guru [Blog](https://springframework.guru/)
* Subscribe to Spring Framework Guru on [YouTube](https://www.youtube.com/channel/UCrXb8NaMPQCQkT8yMP_hSkw)
* Like Spring Framework Guru on [Facebook](https://www.facebook.com/springframeworkguru/)
* Follow Spring Framework Guru on [Twitter](https://twitter.com/spring_guru)
* Connect with John Thompson on [LinkedIn](http://www.linkedin.com/in/springguru)