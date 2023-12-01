# Installation methods

Run the following command to uninstall all conflicting packages:

```
 for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove $pkg; done
```

**1-Set up Docker's apt repository.**

```
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl gnupg
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/debian \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```

**2-Install the Docker packages.(Latest Version)**

```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

**3-Verify that the installation is successful by running the hello-world image:**

```
sudo docker run hello-world
```

# Uninstall Docker Engine

**1-Uninstall the Docker Engine, CLI, containerd, and Docker Compose packages:**
```
sudo apt-get purge docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin docker-ce-rootless-extras
```





**2-Images, containers, volumes, or custom configuration files on your host aren't automatically removed. To delete all images, containers, and volumes:**
```
sudo rm -rf /var/lib/docker
sudo rm -rf /var/lib/containerd
```
