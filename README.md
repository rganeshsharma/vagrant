Use Vagrant for auto provisioning sample Dev K8s clusters 

Versions :

Vagrant Version: 2.3.0 or `sudo dnf install vagrant` or `sudo apt install vagrant` or using `https://www.vagrantup.com/downloads`

VirtualBox Provider Version: 6.1.36r152435 from here : `https://www.virtualbox.org/wiki/Linux_Downloads`
Download GPG and SIG Keys and add them to the system and install depending on you OS distribution.

Vagrantfile defined will deploy : 

Ubuntu 22.04 K8s 1.24.0-00 VM's

Kubernetes 1.24.0-00 (Kubelet, Kubectl, Kubeadm and contraol plane components)

After deployment retrieve the kubeconfig to $HOME/.kube/config using below command 

`scp root@172.16.16.100:/etc/kubernetes/admin.conf $HOME/.kube/config`

once added we can access cluster and deploy the Metrics Server usinjg :

`kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml`

Kubernetes v1.24 Dev Cluster is spinned in minutes!
Use Cases : Client Deno, CKA/CKS Exam prep, POC for DevOps Tools  


Commands to be used:

Vagrant up : for bringing the cluster up

Vagrant status : for status of the cluster
           
Vagrant delete : for cleaning up the cluster
