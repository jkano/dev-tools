# Gitea

Gitea is a community managed lightweight code hosting solution written in Go. It is published under the MIT license.

**Website:** https://gitea.io/en-us/

**Github:** https://github.com/go-gitea/

**Docs:** https://docs.gitea.io/en-us/

## Prerequisites

1. Open the `docker-compose.yml` inside this folder and modify it to meet your needs

## Install instructions

1. Open `Portainer` and log in as `admin`
2. Navigate to `Stacks->Add Stack`
3. Configure your stack as follows:
   ```
   name: gitea
   Build method: Upload from your computer (upload the docker-compose.yml from this folder)
   ```
4. Click on `Deploy the stack`
5. Open `http://<your-ip-or-domain>:9001`
6. Finish gitea setup changing the following options:
   ```
   Domain: change localhost to http://<your-ip-or-domain>
   Port: leave on 3000
   Base url: change from localhost:3000 to http://<your-ip-or-domain>:9001
   ```
7. Access your gitea instance from `http://<your-ip-or-domain>:9001` and register a new user
   
   > NOTE: By default the first registered user will have admin priviledges