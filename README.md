# Microservice Node.js Application on AKS

## Introduction

In the project, I have compeleted the Intro to Kubernetes challenge by What the Hack. Here, this project demonstrates the deployment of a microservice-based Node.js application on Azure Kubernetes Service (AKS). The sample famedical application consists of a **frontend**, a **backend API**, and a **MongoDB database**. It utilizes Kubernetes features such as resource requests, scaling, updates, rollbacks, persistent storage, DNS, and Ingress configurations.

By deploying on AKS, this project ensures scalability, high availability, and efficient management of microservices in a cloud-native environment.

## Table of Contents

- [Features](#features)
- [Project Architecture](#architecture)

## Features

- **Frontend**: A web-based UI for interacting with the application.
- **Backend API**: A Node.js API that serves requests from the frontend and communicates with MongoDB.
- **MongoDB Database**: Stores data for the application.
- **Scalability**: Kubernetes automatically scales the application based on demand.
- **Updates and Rollbacks**: Rolling updates and easy rollbacks implemented for seamless version control.
- **Persistent Storage**: MongoDB data persists even after pods are terminated, thanks to Azure's managed disks.
- **DNS and Ingress**: Configured to allow access to the application via a custom domain name and manage traffic routing.

## Project Architecture
The sample famedical application is composed of three main components:
1. **Frontend** (React or other JavaScript framework)
2. **Backend API** (Node.js/Express)
3. **MongoDB** (Database)

These components are deployed as separate services on Kubernetes, orchestrated via Azure Kubernetes Service (AKS). The Ingress controller routes external traffic to the backend API and frontend, while persistent storage is used to manage MongoDB data.

Below mentioned is the file structure for the project.

```plaintext
.
└── microservices/
    ├── app-v1/
    │   ├── content-api  
    │   └── content-web
    ├── app-v2/
    │   ├── content-api
    │   └── content-web
    ├── env/
    │   ├── azcli.sh
    │   ├── docker.sh
    │   ├── helm.sh
    │   ├── ingress-controller.sh
    │   └── kubectl.sh
    ├── k8s/
    │   ├── v1/
    │   │   ├── api-v1.yml
    │   │   └── web-v1.yml
    │   └── v2/
    │       ├── api-v2.yml
    │       ├── content-init-job.yml
    │       ├── mongo.yml
    │       ├── mongodb-persistent.yml
    │       ├── pvc.yml
    │       └── web-v2.yml
    ├── Document.pdf
    └── README.md
```
The detailed documentation can be found in the Document.pdf file with all the supporting screenshots.

