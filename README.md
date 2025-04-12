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

