[![CircleCI](https://circleci.com/gh/gul-shahzad/udacity-cloud5-kubernetes.svg?style=svg)](https://circleci.com/gh/gul-shahzad/udacity-cloud5-kubernetes)
  
## Project Overview

In this project, we will operationalize a Machine Learning Microservice API. 

For this purpose we will use `sklearn` model, which is provided as skeleton for microservice API. The model has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

Your project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project I have done the following:
* Test the project code using linting
* Complete a Dockerfile to containerize this application
* Deploy the containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested

---
## Files in the project
There are multiple files created in this project. Below you see a brief description of those files. 
* Makefile: The make utility come handy when you want to perform certain tasks to be executed multiple times. In this project we used Makefile to install required libraries, perform tests and lint the application. 
* requirements.txt: This file contains all the dependencies required for the project. 
* Dockerfile: This file contains steps required to run the application in Docker container in local environment. 
* make_prediction.sh: This file contains post request from the app which will make prediction
* upload_docker.sh: Once the docker is runs locally, it's time to tag and upload docker image to Docker hub. Create Docker repo in Docker hub and then use that docker id in this file. 
* run_kubernetes: This file contains code to run the application on kubernetes cluster. I configured the cluster (by installing kubectl and minikube) locally on my system. 
* resize.sh: I also run the proejct on AWS Cloud9. This is handy if you have limited storage in Cloud9, and with this script you can resize the storage of EBS.

## Setup the Environment

* Create a virtualenv and activate it
* Run `make install` to install the necessary dependencies.

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Dockers Steps
1. Install kubectl
2. Install minikube
3. Run in Docker:  `./run_docker.sh`
4. Open another terminal and run:  `./make_prediction.sh`

### Kubernetes Steps

1. Run via kubectl: :  `./run_kubernetes.sh`
2. Open another terminal and run:  `./make_prediction.sh`


