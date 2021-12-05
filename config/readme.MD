# Configuring the webapp service on minikube

## Clone the repository

$ git clone git@github.com:singularityltd/minikube_hello_world.git

## Enter the configuration directory

$ cd minikube_hello_world/config

## Deploy the deployment to minikube 

$  kubectl apply -f ./deployment.yml

## Verify the deployment has successfully been deployed 

$ kubectl get deployments
$ kubectl get pods -l app=singularity-webapp

## Start minikube tunnel to allow access to the cluster

In a separate terminal window :

```bash
$ minikube tunnel
```

## Expose the service, as a LoadBalancer

```bash
$ kubectl expose deployment singularity-webapp --type=LoadBalancer --port=5000
```

## Get the external ip of the deployment, and check with curl

```bash
$ kubectl get svc

NAME                 TYPE           CLUSTER-IP       EXTERNAL-IP      PORT(S)          AGE
kubernetes           ClusterIP      10.96.0.1        <none>           443/TCP          52m
singularity-webapp   LoadBalancer   10.109.142.109   10.109.142.109   5000:30372/TCP   4m7s
```

The flask webapp can be tested by curl, or a browser, using http://10.109.142.109:5000 (replace the IP with the one listed in the deployment)



