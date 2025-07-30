# Docker APT Repository Setup on Ubuntu

This guide describes how to securely set up the official Docker APT repository on an Ubuntu system. This allows you to install and update Docker using `apt`.

## Prerequisites

- Ubuntu-based system (e.g. Ubuntu 20.04, 22.04)
- `sudo` privileges
- Internet connection

## Steps

### 1. Update package index and install required dependencies

```bash
sudo apt-get update
sudo apt-get install ca-certificates curl
```

### 2. Add Docker’s official GPG key

```bash
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc
```

### 3. Set up the Docker APT repository

```bash
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

### 4. Update the APT package index

```bash
sudo apt-get update
```

## Next Steps

After setting up the repository, you can install Docker:

```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

You can verify the installation with:

```bash
docker --version
```

## Post-Installation (Optional)

To run Docker as a non-root user:

```bash
sudo usermod -aG docker $USER
newgrp docker
```

Then verify:

```bash
docker run hello-world
```

---

## References

- [Docker Linux Install Docs](https://docs.docker.com/engine/install/ubuntu/)

## License

This setup script follows the official Docker installation guide and is open for public use.
