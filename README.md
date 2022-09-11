
# Long Way

Loadbalance between two App with HAproxy


## How it works?

Pay attention to the image below


![Long way](https://github.com/SoroushImanian/Long-way/raw/main/pic/Long-way-Soroush-imanian-pic-1.png)

## Environment Variables

To run this project, you will need to add the following environment variables to your Gitlab Project environment:


`NEXUS_USER` --> `"admin"`

`NEXUS_PASSWD` --> `"admin"`

`NEXUS_REGISTRY` --> `"YOUR_Nexus_Server_Host:5000"`

## Install dependencies

Before running the project, we need to install Docker and Docker Compose

###   1. Installing Docker

Download the convenience script for the latest release of Docker CE on Linux from get.docker.com

```bash
  curl -fsSL https://get.docker.com -o get-docker.sh
  sh get-docker.sh
```

After this script finishes running, I always run a test docker command just to see if it’s working or not.

```bash
  docker --version
```

The last step:

```bash
  sudo usermod -aG docker $USER
```

```bash
  sudo systemctl enable docker
```

###   2. Installing Docker Compose

First, confirm the latest version available in their [releases page](https://github.com/docker/compose/releases). At the time of this writing, the most current stable version is `2.10.2`.

Use the following command to download:

```bash
  mkdir -p ~/.docker/cli-plugins/
  curl -SL https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-linux-x86_64 -o ~/.docker/cli-plugins/docker-compose
```

Next, set the correct permissions so that the docker compose command is executable:

```bash
  chmod +x ~/.docker/cli-plugins/docker-compose
```

To verify that the installation was successful, you can run:

```bash
  docker compose version
```
## Run Locally

Clone the project

```bash
  git clone https://github.com/SoroushImanian/Long-way.git
```

Go to the project directory

```bash
  cd Long-way
```

Run Project :

```bash
  docker-compose -f docker-compose.yaml up -d
```
