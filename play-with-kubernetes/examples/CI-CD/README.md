# Kubernetes & CI-CD on Docker for Mac 18.02 CE

Select "minikube' under whale icon > kubernetes & run the below command:

## Start the Minikube

```
minikube start --memory 8000 --cpus 2
```

## Checking the Cluster Information

```
kubectl cluster-info
Kubernetes master is running at https://192.168.99.100:8443

To further debug and diagnose cluster problems, use 'kubectl cluster-info dump'.
[Captains-Bay]🚩 >
```



## Displaying Namespaces

```
kubectl get pods --all-namespaces
kubectl get pods --all-namespaces
NAMESPACE     NAME                                    READY     STATUS    RESTARTS   AGE

default       jenkins-774bf687f9-kwg2f                1/1       Running   0          40m

```
## Installing Jenkins using jenkins.yml, which we’ll use to create our automated CI/CD pipeline. It will take the pod a minute or two to roll out.

```
kubectl apply -f manifests/jenkins.yml
```

```
kubectl rollout status deployment/jenkins
deployment "jenkins" successfully rolled out
```




