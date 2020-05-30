# Docker
#### This repository contains the major functions and commands for practicing Docker for containerizing web applications.

## Docker Installation
Follow the following steps for the installation of Docker on Ubuntu

1. Unstall the older version of Docker
'''
sudo apt-get remove docker docker-engine docker.io containerd runc
'''
2. Update the apt package index and install packages to allow apt to use a repository over
'''
sudo apt-get update

sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common
''' 
3. Add Docker’s official GPG key:
'''
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

'''
4. Verify that you now have the key with the fingerprint
'''
sudo apt-key fingerprint 0EBFCD88
'''
5. 
'''
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
'''
6. 
