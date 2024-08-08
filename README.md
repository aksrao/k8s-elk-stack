# k8s-elk-stack
setting up the monitoring of application using Elastic stack on kubernetes cluster
# Architecture
![Design](/k8s-elk-stack.png)
# Pre-requisites
## Install tools
- kubectl 
- helm
- kind
- docker desktop
## configure tools
- docker desktop (before installing kind cluster )
    - CPU Limit:- 8m 
    - memory Limit:- 6GB
    - virtual disk:- 128GB
## Explaination
- make filebeat (sidecar conatiner) fetch access and error logs of nginx container
- inject the scrapped logs into elasticsearch
- kibana will pull the logs from elasticsearch and the logs will be visible in the dashboard.