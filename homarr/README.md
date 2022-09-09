# Homarr

Simple and lightweight homepage for your server, that helps you easily access all of your services in one place

**Website:** https://homarr.vercel.app/

**Github:** https://github.com/ajnart/homarr

**Docs:** https://homarr.vercel.app/docs/about

## Prerequisites

1. Open the `docker-compose.yml` inside this folder and modify it to meet your needs

2. Download the `default.json` file

3. Modify the `default.json` file to point every service to the correct address:port

4. Login to your instance and create a new folder called `homarr` inside `/home/<user>/Documents`. 

5. Create two more folders inside the created `homarr` folder called `configs` and `icons`

6. Your `homarr` directory should look like this:
    ```
    homarr
     L configs
     L icons
    ```
7. **Optional:** Paste the `default.json` file inside `homarr/configs` folder

## Install instructions

1. Open `Portainer` and log in as `admin`
2. Navigate to `Stacks->Add Stack`
3. Configure your stack as follows:
   ```
   name: homarr
   Build method: Upload from your computer (upload the docker-compose.yml from this folder)
   ```
4. Click on `Deploy the stack`
5. Open `http://<your-ip-or-domain>`
6. If you didn't paste the `default.json` file in configs folder, you can manually add and modify your applications using the UI

> Note: Once you finish with the configuration you can remove the Settings and Add Service button by editing the configuration json file.

To do this, change the line:
```
"customCSS": ".mantine-prtq9m {\ndisplay: flex;\n}\n"
```
to
```
"customCSS": ".mantine-prtq9m {\ndisplay: none;\n}\n"
```