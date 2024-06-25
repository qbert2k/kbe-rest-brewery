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

## Pushing to Docker Hub

```shell
mvn clean package docker:build docker:push
```

## Connect with Spring Framework Guru
* Spring Framework Guru [Blog](https://springframework.guru/)
* Subscribe to Spring Framework Guru on [YouTube](https://www.youtube.com/channel/UCrXb8NaMPQCQkT8yMP_hSkw)
* Like Spring Framework Guru on [Facebook](https://www.facebook.com/springframeworkguru/)
* Follow Spring Framework Guru on [Twitter](https://twitter.com/spring_guru)
* Connect with John Thompson on [LinkedIn](http://www.linkedin.com/in/springguru)

## Kubernetes

### Kubernetes Docker Desktop

```shell
kubectl config get-contexts

kubectl config use-context docker-desktop

kubectl get nodes

kubectl get all
```

### Create Deployment

```shell
kubectl create deployment kbe-rest --image qbert2k/kbe-rest-brewery --dry-run=client -o=yaml > deployment.yml

kubectl apply -f deployment.yml

kubectl get all

docker ps
```

### Create Service

```shell
kubectl create service clusterip kbe-rest --tcp=8080:8080 --dry-run=client -o=waml >> service.yml

kubectl apply -f service.yml

kubectl get all
```

### Port Forwarding

```shell
kubectl port-forward service/kbe-rest 8080:8080

curl http://localhost:8080/actuator/health
```

### Terminating Services and Deployments

```shell
kubectl delete service kbe-rest
kubectl delete deployment kbe-rest

kubectl get all
```