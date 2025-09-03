# 🚀 Kubernetes Cluster Setup on Virtual Machines

This repository contains a step-by-step guide to install a **Kubernetes cluster**  
(1 master + 2 workers) on **Ubuntu 22.04 VMs** using **containerd** and **Calico**.

---

## 📑 Documentation

1. [Prerequisites](docs/01-prerequisites.md)  
2. [Install Container Runtime](docs/02-container-runtime.md)  
3. [Install Kubernetes Components](docs/03-kubernetes-install.md)  
4. [Deploy Calico CNI](docs/04-networking-calico.md)  
5. [Join Worker Nodes](docs/05-worker-nodes.md)  
6. [Troubleshooting](docs/06-troubleshooting.md)  

---

## 🗺️ Cluster Topology

             [ Master Node ]
       (API server, etcd, scheduler, controller)
                /        \
               /          \
      [ Worker01 ]     [ Worker02 ]
 (kubelet, kube-proxy, pods)



