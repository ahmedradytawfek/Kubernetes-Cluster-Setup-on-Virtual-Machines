
---

# 📄 docs/02-network-setup.md


# 🌐 Network Setup & Firewall

## Step 1: Assign Static IP  
**Run on: Master + Worker**

Edit `/etc/netplan/01-netcfg.yaml` and apply:


                  sudo netplan apply
                               network:
                                 version: 2
                                 renderer: networkd
                                 ethernets:
                                   ens18:
                                   dhcp4: no
                                   addresses: [172.20.101.77/23]
                                   gateway4: 172.20.101.254
                                   nameservers:
                                   addresses: [8.8.8.8, 8.8.4.4]

## Step 2: Update /etc/hosts

**Run on: Master + Worker**
 
                127.0.0.1      localhost
                172.20.101.77  k8s-master01
                172.20.101.108 k8s-worker01
                172.20.101.79  k8s-worker02


## Step 3: Open Firewall Ports
**Master Node** 

                    sudo ufw allow 6443/tcp
                    sudo ufw allow 2379:2380/tcp
                    sudo ufw allow 10250/tcp
                    sudo ufw allow 10251/tcp
                    sudo ufw allow 10252/tcp
                    sudo ufw allow 30000:32767/tcp
                    sudo ufw allow 179/tcp
**Worker Nodes** 

                     sudo ufw allow 10250/tcp
                     sudo ufw allow 30000:32767/tcp
                     sudo ufw allow 179/tcp
                     
