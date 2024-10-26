# Jenkins CI/CD Pipeline for Flask Application

This repository demonstrates the setup of a Continuous Integration and Continuous Deployment (CI/CD) pipeline for a Python Flask web application using Jenkins. The pipeline automates the stages of building, testing, and deploying the application.

## Table of Contents
- [Project Overview](#project-overview)
- [Prerequisites](#prerequisites)
- [Pipeline Workflow](#pipeline-workflow)
- [Project Structure](#project-structure)
- [Setup Guide](#setup-guide)
- [Usage](#usage)

## Project Overview
This project uses Jenkins to build a CI/CD pipeline that automates testing and deployment for a simple Flask application. The pipeline performs the following steps:
1. **Build** - Installs dependencies.
2. **Test** - Runs unit tests for the application.
3. **Deploy** - Deploys the application to a production server or local environment.

## Prerequisites
To run this pipeline, ensure you have the following:
- **Jenkins** installed and configured.
- **Python 3.8+** installed.
- **Git** installed for repository management.
- **Flask** installed as the application framework.
- A configured **Jenkins Job** with access to this repository.

## Pipeline Workflow
The pipeline consists of the following stages:
1. **Clone Repository** - Clones this GitHub repository.
2. **Install Dependencies** - Uses `pip` to install dependencies specified in `requirements.txt`.
3. **Run Tests** - Executes unit tests to validate application integrity.
4. **Build and Deploy** - Deploys the Flask application on a target environment.

## Project Structure
```plaintext
Jenkins-CI-CD-pipeline-for-flask-application/
├── app/
│   ├── __init__.py             # Initializes the Flask app
│   ├── main.py                 # Main application file
│   └── tests/
│       ├── test_app.py         # Unit tests
├── requirements.txt            # Python dependencies
├── Jenkinsfile                 # Jenkins pipeline configuration
└── README.md                   # Project documentation

Setup Guide
Follow these steps to set up and run the Jenkins pipeline:

1. Clone the Repository
Clone this repository to your local machine:

git clone https://github.com/AkankshaJairath/Jenkins-CI-CD-pipeline-for-flask-application.git

2. Install Dependencies
Install the required Python dependencies:

pip install -r requirements.txt

3. Configure Jenkins Pipeline
Open Jenkins and create a new Pipeline project.
In the project configuration, point to the repository URL.
Specify the Jenkinsfile in the repository for pipeline configuration.

4. Run the Pipeline
Start the pipeline in Jenkins to automatically trigger build, test, and deployment stages.
Verify that each stage completes successfully.


Usage
After deploying, you can access the application by navigating to:

http://<server-ip>:<port>

