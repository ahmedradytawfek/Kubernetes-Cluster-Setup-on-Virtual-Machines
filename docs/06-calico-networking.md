# 📄 docs/06-calico-networking.md

# 🌐 Deploy Pod Network (Calico)

**Run on: Master**

Apply Calico CNI:

                       kubectl apply -f https://raw.githubusercontent.com/projectcalico/calico/v3.27.3/manifests/calico.yaml

Verify:

                          kubectl get pods -n kube-system

Initially, since only the master is in the cluster, you’ll see Calico pods running only on the master node.
Automatically, Calico schedules a pod on that worker node as CNI run as DaemonSet .
