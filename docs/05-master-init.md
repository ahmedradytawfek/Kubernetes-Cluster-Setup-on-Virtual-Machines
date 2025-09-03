# 📄 docs/05-master-init.md


# 🚀 Initialize Master Node

**Run on: Master only**

Pull images:

                   sudo kubeadm config images pull
                   sudo kubeadm init --pod-network-cidr=192.168.0.0/16


Configure kubectl for user:

                             mkdir -p $HOME/.kube
                             sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
                             sudo chown $(id -u):$(id -g) $HOME/.kube/config
                             
