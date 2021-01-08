# K8S Test Project

My K8S test project with Flask.

## Build the Docker image

Build the application Docker image with 
```
docker build -t eliamanara/flask ./app
```
and push it to your Docker Registry with
```
docker push eliamanara/flask
```

Modify the `eliamanara` in the `k8s` directory in all configuration files containing it.

## Deploy

Deploy with Kubernetes: from the project directory launch
```
kubectl apply -f ./k8s
```

In case you use MicroK8s (as I do on an RPi), try with:
```
microk8s kubectl apply -f ./k8s
```

## Delete

Delete the app with
```
kubectl delete -f ./k8s
```
