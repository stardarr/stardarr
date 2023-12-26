# Stardarr

A Dockerized Homelab Starter kit for you to modify and extend.

## Includes the following services

- Traefik
- Cloudflare Dynamic DNS
- Plex
- Overseer
- Unmanic
- Nextcloud
- Fireshare
- nzbget
- Homarr
- Sonarr
- Radarr
- Readarr
- Bazarr

## Installation

```
git clone https://github.com/stardarr/stardarr.git
cd stardarr
```

## .env files

You **MUST** update all 3 files with your own settings.

- .env
- .env.cloudflare
- .env.nextcloud

## Starting the Services

`docker-compose up -d`

## External Hosts (Optional)

An example dynamic.yml config for Traefik has been provided. You will need to update it with your external domain and IP, and move it to the traefik folder of your app directory.

## Stopping the Services

`docker-compose down`

## Updating the Services

```
docker-compose down
docker-compose pull
docker-compose up -d
```
