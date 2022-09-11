# Taiga

An Agile, Free and Open Source Project Management Tool

**Website:** https://www.taiga.io/es

**Github:** https://github.com/taigaio

**Docs:** https://docs.taiga.io/

## Prerequisites

1. Open the `docker-compose.yml` inside this folder and modify it to meet your needs

2. Login to your instance and create a new folder called `taiga` inside `/home/<user>/`. 

3. Create another folder inside the created `taiga` folder called `taiga-gateway`

4. Create a new file called `taiga.conf` and paste 

## Install instructions

1. Open `Portainer` and log in as `admin`
2. Navigate to `Stacks->Add Stack`
3. Configure your stack as follows:
   ```
   name: taiga
   Build method: Upload from your computer (upload the
   ```
4. Click on `Deploy the stack`
5. Open `http://<your-ip-or-domain>:9003`
6. Finish Taiga configuration