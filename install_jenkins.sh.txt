#!/bin/bash

# Ensure the script runs with sudo
if [ "$(id -u)" -ne 0 ]; then
    echo "Please run as root (use sudo)."
    exit 1
fi


sudo apt update -y

echo "Installing Docker..."
sudo apt install -y docker.io


sudo systemctl start docker
sudo systemctl enable docker


sudo docker pull jenkins/jenkins:lts

echo "Creating Jenkins container on port 8000..."
sudo docker run -d --name jenkins \
    -p 8000:8080 -p 50000:50000 \
    -v jenkins_home:/var/jenkins_home \
    --restart=always \
    jenkins/jenkins:lts

echo "Jenkins is now running on port 8000."
echo "Get the initial admin password with:"
echo "    sudo docker exec jenkins cat /var/jenkins_home/secrets/initialAdminPassword"

