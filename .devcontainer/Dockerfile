# Stage - UV
ARG UV_VERSION=0.5.11
FROM ghcr.io/astral-sh/uv:${UV_VERSION} AS uv_source

# .devcontainer/Dockerfile
FROM python:3.11

# Update the package lists
RUN apt-get update

# Install pip
RUN apt-get install -y python3-pip

# Install uv
COPY --from=uv_source /uv /uvx /bin/

# Install any necessary dependencies
RUN apt-get install -y build-essential libssl-dev libffi-dev python3-dev


RUN uv venv

# # Copy requirements.txt and install the requirements
# COPY requirements.txt .
# RUN pip install -r requirements.txt

# Set the working directory
WORKDIR /workspace