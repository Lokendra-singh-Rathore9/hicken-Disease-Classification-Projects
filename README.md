# Chicken Disease Classification

## Overview

This project focuses on classifying chicken diseases using machine learning and deep learning techniques. By analyzing images of chickens, the model predicts potential diseases, aiding in early detection and prevention.

## Features

Image data preprocessing

Disease classification using deep learning

Model training and evaluation

Performance metrics analysis

Deployment for real-time prediction

## Technologies Used

Python

TensorFlow/Keras

PyTorch (optional)

OpenCV

Scikit-learn

Matplotlib & Seaborn

Docker

DVC (Data Version Control)

AWS & Azure (for cloud deployment)

## Dataset

The dataset consists of labeled images of chickens with different diseases, sourced from:

Kaggle

Research datasets

Manually collected images

## Model Used

Convolutional Neural Networks (CNN)

Transfer Learning (ResNet, VGG16, MobileNet)

Support Vector Machine (SVM) (for comparison)

## Installation

🔹 Clone the repository

 git clone https://github.com/your-username/Chicken-Disease-Classification.git

🔹 Navigate to the project directory

cd Chicken-Disease-Classification

🔹 Create and activate a virtual environment

conda create -n cnncls python=3.8 -y
conda activate cnncls

🔹 Install dependencies

pip install -r requirements.txt

## Usage

🔹 Update configuration files

Update config.yaml
Update secrets.yaml (optional)
Update params.yaml

🔹 Update the entity and configuration manager in src/config

🔹 Update the components and pipeline

🔹 Run the pipeline

python main.py

🔹 Run the application

python app.py

🔹 Open the local host and port to access the model

## DVC Commands

🔹 Initialize DVC

dvc init

🔹 Run the pipeline

dvc repro

🔹 Visualize the DAG

dvc dag

## 🛠️ AWS CI/CD Deployment with GitHub Actions

🔹 Login to AWS console

🔹 Create an IAM user with the following access:

## EC2 access for virtual machines

ECR (Elastic Container Registry) to save Docker images

🔹 Deployment steps:

Build a Docker image of the source code

Push the Docker image to ECR

Launch an EC2 instance

Pull the image from ECR to EC2

Run the Docker image on EC2

🔹 AWS Policies Required:

AmazonEC2ContainerRegistryFullAccess

AmazonEC2FullAccess

🔹 Configure EC2

sudo apt-get update -y
sudo apt-get upgrade
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo usermod -aG docker ubuntu
newgrp docker

🔹 Set up a GitHub self-hosted runner

Go to Settings > Actions > Runners

Add a new self-hosted runner

Follow the instructions to install and configure the runner

🔹 Set up GitHub Secrets

AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_REGION=us-east-1
AWS_ECR_LOGIN_URI=566373416292.dkr.ecr.us-east-1.amazonaws.com
ECR_REPOSITORY_NAME=simple-app

## 🚀 Azure CI/CD Deployment with GitHub Actions

🔹 Build and push the Docker image

docker build -t chickenapp.azurecr.io/chicken:latest .
docker login chickenapp.azurecr.io
docker push chickenapp.azurecr.io/chicken:latest

🔹 Deployment Steps:

Build the Docker image of the source code

Push the Docker image to Container Registry

Launch the Web App Server in Azure

Pull the Docker image from the container registry to the Web App Server and run it

## Results

The model is evaluated using accuracy, precision, recall, and F1-score. The trained model provides a classification report and visualizes predictions.
