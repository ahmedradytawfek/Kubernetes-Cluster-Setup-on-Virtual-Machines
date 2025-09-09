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
       
# Why kubectl tab completion doesn’t work , how can solve this ?
**on: Master**

First, install bash-completion (if not already installed):

Ubuntu/Debian:

           sudo apt-get install bash-completion -y

Then add this to your ~/.bashrc:

           source <(kubectl completion bash)


Add the alias to your shell config file :

         echo "alias k=kubectl" >> ~/.bashrc
         echo "source <(kubectl completion bash)" >> ~/.bashrc
         echo "complete -F __start_kubectl k" >> ~/.bashrc
         
Reload:

          source ~/.bashrc
         
