This repository is the kubernetes manifest for an application 
and url for the github repository of that application is `https://github.com/evans22j/Budget-App`

This repository contain 3 files namely :-
- deployment.yaml
- statefulset.yaml
- ingress.yaml

deployment.yaml file contain the the main application deployment whose image is comming from DockerHub `yashsharma127/budget-app-web`

statefulset.yaml contain the database setup whose image is comming from DockerHub `yashsharma127/postgres-db-image`

ingress.yaml contain routing of both the container services i.e application and database.