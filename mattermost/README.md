# Mattermost

Open source platform for secure collaboration across the entire software development lifecycle

**Website:** https://mattermost.com/

**Github:** https://github.com/mattermost/mattermost-server

**Docs:** https://docs.mattermost.com/

## Prerequisites

1. Open the `docker-compose.yml` inside this folder and modify it to meet your needs

2. Download the `env` file

3. Modify the `env` file and modify Domain, user and passwords

## Install instructions

1. Open `Portainer` and log in as `admin`
2. Navigate to `Stacks->Add Stack`
3. Configure your stack as follows:
   ```
   name: mattermost
   Build method: Upload from your computer (upload the `docker-compose.yml` from this folder)
   Environment variables: Change to advanced mode and paste the contents of the `env` file you downloaded before
   ```
4. Click on `Deploy the stack`
5. Open `http://<your-ip-or-domain>:9002`
6. Finish Mattermost configuration