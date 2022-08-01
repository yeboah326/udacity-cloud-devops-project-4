[![CircleCI](https://dl.circleci.com/status-badge/img/gh/yeboah326/udacity-cloud-devops-project-4/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/yeboah326/udacity-cloud-devops-project-4/tree/main)

## Project Overview

In this project, I was required to apply the skills I acquired in the Udacity Nanodegree Programme to operationalize a Machine Learning Microservice API. 

I was given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. This project tested my ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. 


### Files in repository
**.circleci/config.yml** - contains the configuration of the for jobs in circleci
**model_data** - contains the trained AI model and the training data
**app.py** - contains the api which generates predictions through the endpoints
**Dockerfile** - contains instructions on how the docker image will be created
**make_prediction.sh** - a bash script that will access the api with a payload for a prediction
**Makefile** - contains the mini scripts that can be run in the repo
**requirements.txt** - contains the dependencies of the project
**run_docker.sh** - contains code that runs the docker image locally
**run_kubernetes.sh** - contains code that runs the api on a kubernestes cluster locally
**upload_docker.sh** - contains code that uploads the docker container to docker hub
---

## Setup the Environment

* Create a virtualenv with Python 3.7 and activate it. Refer to this link for help on specifying the Python version in the virtualenv. 
```bash
python3 -m pip install --user virtualenv
# You should have Python 3.7 available in your host. 
# Check the Python path using `which python3`
# Use a command similar to this one:
python3 -m virtualenv --python=<path-to-Python3.7> env
source env/bin/activate
```
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
