
# Application Deployment on Minikube Cluster

In this project I taken tg-redirect project from github and I used frontend of this application to deploy it on Minikube Cluster.

This project is based on frontend application deployment on Minikube clusetr using kubernetes.
## Project Description

1. Created Dockerfile for building the docker image of application.
2. Deployed craeted image to my personal docker hub repository.
3. Created yaml files for deploying the application.
4. Created pod.yaml file for deploying the image of application on the Minikube cluster.
5. Created deployment.yaml file for deploying the multiple copies of images (replicas) of the application on the Minikube cluster.
6. Created service.yaml file of nodeport type for accessing the application locally.
7. After creating the files deployed it to the minikube cluster using kubectl commands.
8. Get IP address of the service using minikue command and accessed it locally.
## Tools

During the project I used the Lens IDE for monitoring the minikube cluster.
Using this IDE you can manage the pods, deploymets and services, etc. using this graphical inteface.

![Lens](https://github.com/prajapatdip/Kubernetes-first/assets/104031556/59ab3812-90f1-4b76-9659-6223f33e29e1)

## Run Locally

```
    git clone https://github.com/prajapatdip/Kubernetes-first.git
    cd Kubernetes-first
```
Install the minikube and kubectl cli through the folliwing documentation:

```
Minikube: https://minikube.sigs.k8s.io/docs/start
kubectl CLI: https://kubernetes.io/docs/tasks/tools
```

Deploying the application to the minikube.

```
    cd k8s
    kubectl apply -f deployment.yaml
    kubectl apply -f service.yaml
```

Checking the Deployment and Service is runnig

```
    kubectl get all
```

Getting the URL from Minikube cluster.

```
    minikube service my-service --url
```
Copy the URL and past it on any browser to run the application.

![api](https://github.com/prajapatdip/Kubernetes-first/assets/104031556/68338a81-a572-4008-bd9f-4cb4ae3d416b)

Docker image: https://hub.docker.com/repository/docker/prajapatdip/tg-redirect/general
