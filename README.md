# library-webserver

This is a study case on how to approach the container creation and architecture for a Spring Boot app as a DevOps engineer using an nginx reverse proxy to the Java backend and a mariadb for writing data.

This app works in conjunction with repos

*library-db
*library-backend-api

1. Library DB should get started first
2. Library Backend API should get started second
3. Lastly, we start Library Webserver


### Step #3 to run Library Webserver

1. Deploy kubernetes deployment and services
```
kubectl apply -f .
```

2. Run a port forward to expose a port on your local
```
kubectl port-forward service/library-webserver-service 8080:80
```
