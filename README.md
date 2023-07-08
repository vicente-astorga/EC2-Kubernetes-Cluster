## Kubernetes Cluster with Terraform and Ansible from Gitlab CI on AWS EC2

This project uses three EC2 instances, one master and two workers to build a Kubernetes cluster using Kubeadm. The instances are part of a *security group* that allows traffic between them through the multiple necessary ports (for example *etcd* (2379-2380), *API Server* (6443), *kubelet (10250), kube-proxy (10257), kube-scheduler (10259)* and *services* *(30000-32767)*). The creation of the infrastructure is done using Terraform and the configuration of the environment and the provisioning of the cluster with Ansible. The deployment of a Spring-Mongo application whose access is through a NodePort was carried out. This in turn uses a volume for storage and persistence of the Mongo database. Finally, Prometheus is used with Grafana to be able to observe cluster metrics, in terms of performance and operability.

#### Repository
https://gitlab.com/vicente-astorga/ec2-kubernetes-cluster

#### Pipeline execution
https://gitlab.com/vicente-astorga/ec2-kubernetes-cluster/-/pipelines/903808813

![Alt text](/diagrama.jpg "Image")
