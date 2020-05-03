[![CircleCI](https://circleci.com/gh/amitnike/udacity-project4-microservice-kubernetes.svg?style=svg)](https://circleci.com/gh/amitnike/udacity-project4-microservice-kubernetes)

## Project Overview

Running the application
Standalone:

## Setup a python virtual environment and activate it

python3 -m venv ~/.devops
source ~/.devops/bin/activate

## Install the necessary dependencies

make install

## Run the main application

python app.py
Run in Docker: ./run_docker.sh
Run in Kubernetes: ./run_kubernetes.sh


## Predict housing prices

While the application is running, run ./make_predicion.sh to make calls to the API

## Upload Docker image to DockerHub

After running ./run_docker.sh, execute script./upload_docker.sh to upload image to DockerHub

## Project Files

app.py: The Flask API
requirements.txt: Prerequisites of Python packages for Flask API to run
model_data/boston_housing_prediction.joblib: Pretrained sklearn model for the API
Dockerfile: Defines the container in which the API runs
Makefile: Commands to install and lint the applicaiton
run_docker.sh: Runs the API in a Docker container (defined by Dockerfile)
run_kubernetes.sh: Runs the API as a Kubernetes deployment
make_prediction.sh: When the applicaiton is running, this script can be run to make a call to the API and generate a prediciton
upload_docker.sh: Tags and uploads the Docker image to DockerHub
output_txt_files/docker_out.txt: Console output from running run_docker.sh and make_prediction.sh
output_txt_files/kubernetes_out.txt Console output from running run_kubernetes.sh and make_prediction.sh
.circleci/config.yml: Defines the circleCI deployment
