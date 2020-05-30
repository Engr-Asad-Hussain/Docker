# Docker
#### This repository contains the major functions and commands for practicing Docker for containerizing web applications.

## Docker Installation
Follow the following steps for the installation of Docker on Ubuntu

1. Uninstall the older version of Docker if you have previously installed docker on your system.
```
sudo apt-get remove docker docker-engine docker.io containerd runc
```
2. Update the apt package index and install packages to allow apt to use a repository over.
```
sudo apt-get update
```
```
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common
```
3. Add Docker’s official GPG key:
```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```
4. Now make sure to verify that GPG key is installed properly
```
sudo apt-key fingerprint 0EBFCD88
```
5. Use the following command to set up the stable repository.
```
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
```
6. Update the apt package index, and install the latest version of Docker Engine.
```
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
```
7. Verify that Docker Engine is installed correctly by running the hello-world image.
```
sudo docker run hello-world
```
