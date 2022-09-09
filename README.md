[![CircleCI](https://dl.circleci.com/status-badge/img/gh/Degoke/operationalize-ml-api/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/Degoke/operationalize-ml-api/tree/main)

## Project Overview

This project operationalizes a Machine Learning Microservice API. 

Given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

The following tasks were performed:
* Test project code using linting
* Complete Dockerfile to containerize the application
* Deploy the containerized application using Docker and make a prediction
* Improve the log statements in the source code
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested


---
### Short description of folders and files in the repo

* [.circleci](/Project_4_Operationalize_ML_API/.circleci): For the CircleCI build server
* [model_data](/Project_4_Operationalize_ML_API/model_data) : this folder contains the pretrained `sklearn` model and housing csv files
* [output_txt_files](/Project_4_Operationalize_ML_API/output_txt_files): folder contains sample output logs from running `./run_docker.sh` and `./run_kubernetes.sh`
* [app.py](/Project_4_Operationalize_ML_API/app.py) : contains the flask app
* [Dockerfile](/Project_4_Operationalize_ML_API/app.py): contains instructions to containerize the application
* [Makefile](/Project_4_Operationalize_ML_API/Makefile) : contains instructions for environment setup and lint tests
* [requirements.txt](/Project_4_Operationalize_ML_API/requirements.txt): list of required dependencies
* [run_docker.sh](/Project_4_Operationalize_ML_API/run_docker.sh): bash script to build Docker image and run the application in a Docker container
* [upload_docker.sh](/Project_4_Operationalize_ML_API/upload_docker.sh): bash script to upload the built Docker image to Dockerhub
* [run_kubernetes.sh](/Project_4_Operationalize_ML_API/run_kubernetes.sh): bash script to run the application in a Kubernetes cluster
* [make_prediction.sh](/Project_4_Operationalize_ML_API/make_prediction.sh): bash script to make predictions against the Docker container and k8s cluster
* [README.md](/Project_4_Operationalize_ML_API/README.md): this README file

### Instructions
## Setup the Environment

* Create a virtualenv and activate it
1. Run `python3 -m venev ~/.devops`
2. Run `source ~/.devops/bin/activate`
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl
