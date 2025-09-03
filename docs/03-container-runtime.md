
---

# 📄 docs/03-container-runtime.md


# 🐳 Install Container Runtime (containerd)

**Run on: Master + Worker**

Update and install dependencies:

                 sudo apt-get update
                 sudo apt-get install -y ca-certificates curl gnupg lsb-release

# Add Docker repo for containerd:

                              sudo mkdir -m 0755 -p /etc/apt/keyrings
				           	  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg                      
                              echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] \
                              https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | \
                              sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
# Install containerd:
                      sudo apt-get update
                      sudo apt-get install -y containerd.io

# Configure systemd cgroup:

                          sudo mkdir -p /etc/containerd
                          containerd config default | sudo tee /etc/containerd/config.toml
                          sudo sed -i 's/SystemdCgroup = false/SystemdCgroup = true/' /etc/containerd/config.toml
                          sudo systemctl restart containerd
                          sudo systemctl enable containerd

