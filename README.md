# Overview #
This project creates a simple API that runs on a docker container.
The goal of the project is to use kubernetes with skaffold to build+deploy
the container.

## Build the Container ##
````
docker build -t "repo/tag" .
````
Now we can scan the container with Snyk.
```
docker scan --login
```
The command will open a web browser window and take you to the Snyk login page.  If you don't
have an account, create one they are free.  Now we will be able to scan the docker image.
```
docker scan
```
## More to Come ##
kubectl create deployment fastapi-service --image=fastapi-hw --dry-run=client -o
 yaml >deployment.yaml
