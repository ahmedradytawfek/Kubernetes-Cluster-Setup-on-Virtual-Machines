# 🚀 Kubernetes Cluster Setup on Virtual Machines

This repository provides a **step-by-step guide** to install a Kubernetes cluster  
(1 master + 2 workers) on **Ubuntu 22.04 VMs** using **containerd** and **Calico**.  

Each step of the installation is documented separately for clarity.  

---

## 📑 Documentation

1. [🛠 Prerequisites](docs/01-prerequisites.md)  
2. [🌐 Network Setup & Firewall](docs/02-network-setup.md)  
3. [🐳 Install Container Runtime (containerd)](docs/03-container-runtime.md)  
4. [⎈ Install Kubernetes Components](docs/04-kubernetes-components.md)  
5. [🚀 Initialize Master Node](docs/05-master-init.md)  
6. [🌐 Deploy Calico Networking](docs/06-calico-networking.md)  
7. [👷 Join Worker Nodes](docs/07-join-workers.md)  
8. [🛠 Troubleshooting](docs/08-troubleshooting.md)  


---

## 🗺️ Cluster Topology

             [ Master Node ]
       (API server, etcd, scheduler, controller)
                /        \
               /          \
      [ Worker01 ]     [ Worker02 ]
 (kubelet, kube-proxy, pods)


