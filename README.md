# Installing Docker On Proxmox ?
Docker is an apllication or a program that runs over and operating system, its not an operating system by it self yet, so in order to install docker first we need to have an operating system, and the key to this is to install a container named turnkey core, then install docker over it.

1. install turnkey core
2. install sudo command
3. install docker
5. install docker compose
6. install portainer

## Install Sudo
```
apt-get install sudo
```

## Install Docker
```
sudo apt install docker.io
sudo systemctl enable docker
sudo systemctl start docker
sudo systemctl status docker
```

## Install Docker Compose
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

## Install Portainer
```
sudo docker run -d \
--name="portainer" \
--restart on-failure \
-p 9000:9000 \
-v /var/run/docker.sock:/var/run/docker.sock \
-v portainer_data:/data \
portainer/portainer-ce
```
