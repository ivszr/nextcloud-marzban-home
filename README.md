# nextcloud-marzban-home
Thx https://github.com/Jolymmiles/confluence-marzban-home/

<img width="1920" height="949" alt="loginpage" src="https://github.com/user-attachments/assets/4057b57a-1b60-40a2-a646-3a09d7e8c365" />



# Installation Guide for Marzban Home Template

This guide provides step-by-step instructions for setting up the Marzban home template on a Debian-based system.

## Before you begin, ensure you have the following:

- A Debian-based operating system.
- `wget` installed. If not, you can install it using the following commands:

  ```bash
  sudo apt-get update
  sudo apt-get install wget

## Step 1: Create Necessary Directories

First, you'll need to create the necessary directories for the Marzban home template.

Open your terminal and run the following command:

```bash
sudo mkdir -p /var/lib/marzban/templates/home/
```

This command will create all the required directories in the path `/var/lib/marzban/templates/home/`.

## Step 2: Download the Template File

Next, download the `index.html` template file from the GitHub repository and save it in the created directory.

Run the following command:

```bash
sudo wget https://raw.githubusercontent.com/ivszr/nextcloud-marzban-home/refs/heads/main/index.html
```

This command will download the `index.html` file and place it in the `/var/lib/marzban/templates/home/` directory.

## Step 3: Marzban .env

```bash
nano /opt/marzban/.env
```

Set CUSTOM_TEMPLATES_DIRECTORY to "/var/lib/marzban/templates/"
```
CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"
```

## Step 4: Restart Marzban

```bash
marzban restart
```
