# Developer tools

These developer tools should be installed on Linux (Ubuntu). If using other OS like Windows you should install Docker Desktop for Windows, then follow the instructions to install Portainer on Windows. Other developer tools can be installed from Portainer.

## Prerequisites 

### Docker

Install docker on Ubuntu:

1. Open a terminal and run the following commands to install prerequisites:
   
- ```
  sudo apt-get update
  ```
- ```
  sudo apt-get install ca-certificates curl gnupg lsb-release
  ```
- ```
  sudo mkdir -p /etc/apt/keyrings
  ```
- ```
  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
  ```
- ```
  echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
  ```

2. Now run these commands to install docker:
- ```
  sudo apt-get update
  ```
- ```
  sudo apt-get install docker-ce docker-ce-cli containerd.iodocker-compose-plugin docker-compose
  ```
- ```
  sudo groupadd docker
  ```
- ```
  sudo usermod -aG docker $USER
  ```
- ```
  newgrp docker
  ```

3. If not enabled, you can enable Docker to start on boot with:
- ```
  sudo systemctl enable docker.service
  ```
- ```
  sudo systemctl enable containerd.service
  ```

## Portainer

Portainer is the tool used to manage your containers and install/update/remove them.

### Install

1. Open a terminal and run:
- ```
  docker volume create portainer_data
  ```
- ```
  docker run -d -p 8000:8000 -p 9443:9443 -p 9000:9000 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest
  ```

    >Note: You can change the port 9000 (http) and 9443 (https) to different ones if you want to access your instance from a different port. (i.e. -p 9001:9000 to access portainer via http port 9001)

2. You can access your portainer instance using `http://<your-ip-or-domain>:9000` or `https://<your-ip-or-domain>:9443`

    > Note: It is normal when accessing via https to have a untrusted certificate as we havent added one yet.

3. Log into your Portainer instance, create an admin and password user.
   
4. If you want to add an SSL certificate to your instance, go to `Settings->SSL certificate` and upload a X.509 certificate, commonly a crt, a cer, or a pem file using the provided option.

5. Following tools installations will be done from portainer

## Developer Tools

- [Gitea](gitea/README.md)
- [Mattermost](mattermost/README.md)
- [Taiga](taiga/README.md)
- [Homarr](homarr/README.md)