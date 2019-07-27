# jenkins_docker_unittests
Unit tests running in a Python 3.7.2 Docker Image triggered by a Jenkins Pipeline. Consider it my implementation from another example as well as my personal notes from the quoted Medium article at the end of this README file.
It is provided without any warranties and I'm not responsable for any damage, so use it carefully by your own risk. ;)

## First things first

This is a simple example of a Jenkinsfile for a Jenkins pipeline. It's intention is to allow Python developers to understand unit tests and how they run in a Jenkins scenario generating a Docker container.

## What you will need

A little bit of docker and Jenkins knowledge.
Jenkins installed or Jenkins container running with docker installed inside it and if you work offline you will need the docker image of Python 3.7.2 on your computer.

The files to run the test:

- app.py: Is the python application, in this case runs a simple web example using Flask.
- tests.py: This program run the unit tests.
- requirements.txt: Are the libraries to be implemented before running the tests.

## Implementation

1. Clone this repo.
2. Generate your working directory in case you use local containerized Jenkins image, I've named mine z_python_pipeline.
3. Copy the app.py, Jenkinsfile, requirements.txt and tests.py to your working directory (you can map your local folder to your Jenkins contianer if you want). In my case /jenkins/jenkins_home/workspace/z_python_pipeline.


Thanks to Joaquin Menchaca for his post which is the same example but detailed and better explained  https://medium.com/@Joachim8675309/jenkins-ci-pipeline-with-python-8bf1a0234ec3