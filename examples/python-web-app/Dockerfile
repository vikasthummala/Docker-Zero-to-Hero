FROM ubuntu:latest

# Set the working directory
WORKDIR /app

# Install system dependencies
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
       python3 \
       python3-pip \
    && rm -rf /var/lib/apt/lists/*

# Copy requirements.txt file
COPY requirements.txt /app/

# Install Python dependencies
RUN pip3 install --no-cache-dir -r requirements.txt

# Copy project files
COPY devops /app/devops

# Set the working directory to devops
WORKDIR /app/devops
