# Creating AWS EKS Cluster:
* This repo is for creating an AWS EKS cluster with 3 nodes as its desired Capacity
* Create an EKS cluster from the config file via yaml
  ```
  eksctl create cluster -f eks.yaml
  ```
* To create a cluster directly without a file
  ```
  eksctl create cluster --name expense-1

* you can use the specific resources like which VPC, you should use or which resource you need to add? All you can mention in the cluster config file which is eks.yaml

* To delete the eks cluster
```
eksctl delete cluster -f eks.yaml
```
* Use the --dry-run functionality to disply the config file and highlight if any errors. The dry-run option will not create a cluster.

* When a ClusterConfig file is passed with --dry-run, eksctl will output a ClusterConfig file containing the values set in the file.
```
$ eksctl create cluster -f eks.yaml
```
* Install Kubectl on linux
```
  curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
  curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl.sha256"
  echo "$(cat kubectl.sha256)  kubectl" | sha256sum --check
  sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
  kubectl version --client
```

* Install Kubens on linux
```
sudo git clone https://github.com/ahmetb/kubectx /opt/kubectx
sudo ln -s /opt/kubectx/kubens /usr/local/bin/kubens
echo "source /opt/kubectx/completion/kubens.bash" >> ~/.bashrc
```

