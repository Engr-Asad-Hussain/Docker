# Installation of Kubernetes
Follow the steps below to install kubernetes:

1. To check if virtualization is supported on Linux, run the following command and verify that the output is non-empty:
```
grep -E --color 'vmx|svm' /proc/cpuinfo
```

## Install and Set Up kubectl
2. Make sure you have kubectl installed. You can install kubectl according to the instructions
```
sudo apt-get update && sudo apt-get install -y apt-transport-https gnupg2
curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
echo "deb https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee -a /etc/apt/sources.list.d/kubernetes.list
sudo apt-get update
```
Now kubectl has installed check the version of kubectl using:
```
kubectl version
```
## Install a Hypervisor (VirtualBox)
3. In order to install the latest VirtualBox, you need to have the Multiverse repository enabled on your system
```
sudo add-apt-repository multiverse && sudo apt-get update
```
4. Now, enter the following command to install VirtualBox:
```
sudo apt install virtualbox
```
The system will prompt you with a Y/n option in order to begin the installation procedure. Please enter Y and hit Enter to begin. VirtualBox will then be installed on your system.
5. You can launch VirtualBox directly through the Terminal by entering the following command:
```
virtualbox
```
## Install Minikube
6. Type the following command one by one to install Minikube:
```
curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
chmod +x minikube
```
Here's an easy way to add the Minikube executable to your path
```
sudo mkdir -p /usr/local/bin/
sudo install minikube /usr/local/bin/
```
7. Now minikube and kubectl has been installed verify it using:
```
minikube version
kubectl version
```
8. Now run the command to start minikube:
minikube start
```
Once when you typed the ```minikube start``` command and it shows an type of error. Then first delete the minikube using ```minikube delete``` and then start again.
