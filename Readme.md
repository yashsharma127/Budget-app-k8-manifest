This repository is the kubernetes manifest for an application 
and url for the github repository of that application is `https://github.com/evans22j/Budget-App`

This repository contain 3 files namely :-
- deployment.yaml
- statefulset.yaml
- ingress.yaml

all the configuration files are written under namespace `budget-app` ensuring that all resources are deployed within the same namespace.

deployment.yaml file contain the the main application deployment whose image is comming from DockerHub `yashsharma127/budget-app-web` and furthure creating the service for application using NodePort

statefulset.yaml contain the database setup whose image is comming from DockerHub `yashsharma127/postgres-db-image` and furthur creating a service for the database using NodePort

ingress.yaml configuring routing for both the container services i.e application and database.

## To set up and run the project on your Kubernetes cluster follow these steps.

1. Clone this repository:
    `git clone https://github.com/yashsharma127/Budget-app-k8-manifest.git`

2. Navigate to the project directory:
    `cd Budget-app-k8-manifest`

# Accessing the Application

1. Apply the provided YAML files to your cluster:

`kubectl apply -f deployment.yaml`
`kubectl apply -f statefulset.yaml`
`kubectl apply -f ingress.yaml`

2. Wait for the resources to deploy, and ensure they are running:

`kubectl get pods -n budget-app`
`kubectl get services -n budget-app`
`kubectl get ingress -n budget-app`


3. Access the application through the Ingress endpoint (replace budget-app.info with   your actual domain or IP address in ingress.yaml):
    `http://budget-app.info`

