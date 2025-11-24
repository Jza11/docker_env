# Dockerfile used to setup the environment to interact with ML models
# It will have scikit-learn and Pytorch as main libraries installed.
# Author: Jza11 (josemiguelcaceb@gmail.com)

# From Ubuntu image 
FROM ubuntu:24.04

#Update packages
RUN apt update 

# Install python3 and pip (Depends if we create venv or not)
RUN apt install -y python3 pip

# Install venv command
RUN apt install -y python3.12-venv

# Make a project for scikit-learn 
WORKDIR /frameworks/

# Enter the folder and create the virtual environment and install dependencies
RUN python3 -m venv /opt/ml-venv

# Enable the Virtual Environment 
ENV PATH="/opt/ml-venv/bin:$PATH"

# Install sklearn library
RUN pip3 install -U scikit-learn

# Install pytorch
RUN pip3 install torch torchvision --index-url https://download.pytorch.org/whl/cpu








