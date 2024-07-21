# jenkins-on-kubernetes

I am learning about deploying Jenkins to Kubernetes with persistent volume.

## Create namespace for jenkins
´´´sh
kubectl create ns jenkins
´´´

## Run the Kubernetes configuration in the root of this repository
´´´sh
kubectl -n jenkins apply -f ./
´´´

## Get pods in jenkins namespace and copy the name of the pod running
´´´sh
kubectl get pods -n jenkins
´´´

## Get initial Jenkins password from logs
´´´sh
kubectl -n jenkins logs <pod-name>
´´´

## Port forward Jenkins UI to localhost:8080
´´´sh
kubectl -n jenkins port-forward <pod-name> 8080
´´´

## Enter the password to UI

## Install suggested plugins

## Configure Jenkins
https://www.jenkins.io/doc/book/