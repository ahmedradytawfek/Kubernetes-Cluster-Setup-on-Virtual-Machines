# 📄 docs/07-join-workers.md

# 👷 Join Worker Nodes

**Run on: Worker nodes**

After running kubeadm init on the master, a kubeadm join command is generated. Run this command on each worker node to securely connect it to the cluster :


                    sudo kubeadm join 172.20.101.77:6443 --token <token> \
                        --discovery-token-ca-cert-hash sha256:<hash>

**Check from master:**

                            kubectl get nodes


✅ Expected output (example with one master and two workers):

                          NAME           STATUS   ROLES           AGE   VERSION
                          k8s-master01   Ready    control-plane   20m   v1.30.0
                          k8s-worker01   Ready    <none>          10m   v1.30.0
                          k8s-worker02   Ready    <none>          5m    v1.30.0
