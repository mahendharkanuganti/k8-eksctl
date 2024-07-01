# Creating AWS EKS Cluster:
* This repo is for creating an AWS EKS cluster with 3 nodes as its desired Capacity
* Create an EKS cluster from the config file via yaml
  ```
  eksctl create cluster -f eks.yaml
  ```
* To create a cluster directly without a file
  ```
  eksctl create cluster --name expense-1