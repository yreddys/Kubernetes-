Kubectl installation

1. Update package list
~~~groovy
sudo apt-get update
~~~
2. Install transport & curl
~~~groovy
sudo apt-get install -y apt-transport-https ca-certificates curl gnupg
~~~
 3. Add Google Cloud public signing key
~~~groovy
curl -fsSL https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
~~~
4. Add the Kubernetes APT repo
~~~groovy
echo "deb https://apt.kubernetes.io/ kubernetes-xenial main" | \
sudo tee /etc/apt/sources.list.d/kubernetes.list
~~~


 5. Install kubectl
~~~groovy
sudo apt-get install -y kubectl
~~~
 If it still fails, just go with Snap (Quick Fix)
~~~groovy
sudo snap install kubectl --classic
~~~

Minikube Installation 

 1. Update package list
~~~groovy
sudo apt-get update -y
~~~
2. Install dependencies
~~~groovy
sudo apt-get install -y curl wget apt-transport-https
~~~
 3. Download Minikube binary
~~~groovy
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
~~~
4. Install the binary
~~~groovy
sudo install minikube-linux-amd64 /usr/local/bin/minikube
~~~
5. Check installation
~~~groovy
minikube version
~~~
 Install Virtualization Driver (Docker is recommended)
~~~groovy
sudo apt-get install -y docker.io
sudo usermod -aG docker $USER
newgrp docker
~~~
Start Minikube
~~~groovy
minikube start --driver=docker

~~~
To run a Pod 

 open or create a file named pod.yml
~~~groovy
vi pod.yml

~~~
 create Kubernetes resources (like Pods, Deployments, or Services) from a configuration file written in YAML.
~~~groovy
kubectl create -f pod.yml
~~~

 List all the pods 
 ~~~groovy
kubectl get pods -o wide

~~~

open a terminal inside the Minikube virtual machine
 ~~~groovy
minikube ssh

 ~~~

 command-line tool used to make HTTP requests.
 ~~~groovy
curl <IP_ADDRESS>

~~~

