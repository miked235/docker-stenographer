# Stenographer Docker Container

## Docker

For deploying Stenographer within a Docker container, please first confirm your network interface and port number in the ```config``` and ```Dockerfile``` before continuing. 

To run Stenographer, please use the command below (remember to change the port):
```
sudo docker run -p 1234 -itd --cap-add NET_RAW --cap-add NET_ADMIN --cap-add IPC_LOCK --name stenographer stenographer
```

## Kubernetes

For deploying Stenographer on a Kubernetes cluster, you will need to use a configmap for the ```config``` file and place it in ```/etc/stenographer/config```. Additionally, you will need to add the following capabilities:

* NET_ADMIN
* NET_RAW
* IPC_LOCK


If you're looking for more opensource containerized tools, take a look at https://github.com/sealingtech/EDCOP for a fully automated network security platform that utilizes Docker and Kubernetes for deployments and scaling!
