# 📄 docs/06-calico-networking.md

# 🌐 Deploy Pod Network (Calico)

**Run on: Master**

Apply Calico CNI:

                       kubectl apply -f https://raw.githubusercontent.com/projectcalico/calico/v3.27.3/manifests/calico.yaml

Verify:

                          kubectl get pods -n kube-system
