# .devcontainer/Dockerfile
FROM python:3.11

# Update the package lists
RUN apt-get update

# Install pip
RUN apt-get install -y python3-pip

# Install any necessary dependencies
RUN apt-get install -y build-essential libssl-dev libffi-dev python3-dev

# # Copy requirements.txt and install the requirements
# COPY requirements.txt .
# RUN pip install -r requirements.txt

# Set the working directory
WORKDIR /workspace