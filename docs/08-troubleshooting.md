# 📄 docs/08-troubleshooting.md

# 🛠 Troubleshooting

## Node NotReady
**Check on: Node**

          journalctl -u kubelet -f

# CNI Not Initialized
**Check on: Master**

         kubectl get pods -n kube-system

# Disk Errors
**Check on: Node**

          sudo systemctl restart containerd
       
