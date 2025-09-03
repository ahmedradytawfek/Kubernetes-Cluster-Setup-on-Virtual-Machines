# 🛠 Prerequisites

## Operating System
- Ubuntu 22.04 LTS (fresh install recommended)

## Hardware Requirements
- Master Node: 2 CPU, 4 GB RAM, 20 GB disk  
- Worker Nodes: 2 CPU, 2 GB RAM, 20 GB disk  

## Networking
- All nodes on the same subnet with static IPs  
- Internet access for package and image downloads  
- Proper DNS or `/etc/hosts` resolution between nodes  
- Firewall ports open for Kubernetes  

## Software
- `openssh-server` installed  
- `ufw` firewall configured  
- **Swap disabled** permanently  
- `containerd` runtime with **systemd cgroup driver**  
