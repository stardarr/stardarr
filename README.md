# Stardarr

A Dockerized Homelab Starter kit for you to modify and extend.

## Includes the following services

- [Traefik](https://github.com/traefik/traefik)
- [Cloudflare Dynamic DNS](https://github.com/oznu/docker-cloudflare-ddns)
- [Plex](https://www.plex.tv/)
- [Overseer](https://overseerr.dev/)
- [Unmanic](https://docs.unmanic.app/)
- [Nextcloud](https://nextcloud.com/)
- [Fireshare](https://github.com/ShaneIsrael/fireshare)
- [NZBGet](https://nzbget.net/)
- [Homarr](https://homarr.dev/)
- [Sonarr](https://sonarr.tv/)
- [Radarr](https://radarr.video/)
- [Readarr](https://readarr.com/)
- [Bazarr](https://www.bazarr.media/)

## Installation

```
git clone https://github.com/stardarr/stardarr.git
cd stardarr
~ edit the .env files ~
docker-compose up -d
```

## .env files

You **MUST** update all 3 files with your own settings.

- .env
- .env.cloudflare
- .env.nextcloud

# Service URLs

| Service   | URL                  |
| --------- | -------------------- |
| Plex      | plex.domain.com      |
| Overseerr | overseerr.domain.com |
| Nextcloud | cloud.domain.com     |
| Fireshare | videos.domain.com    |
| NZBGet    | localhost:6789       |
| Unmanic   | localhost:8888       |
| Homarr    | localhost:7575       |
| Sonarr    | localhost:8989       |
| Radarr    | localhost:7878       |
| Readarr   | localhost:8787       |
| Bazarr    | localhost:6767       |

# Commands

### Starting the Services

`docker-compose up -d`

### Stopping the Services

`docker-compose down`

### Updating the Services

```
docker-compose down
docker-compose pull
docker-compose up -d
```

## External Hosts (Optional)

An example dynamic.yml config for Traefik has been provided. You will need to update it with your external domain and IP, and move it to the traefik folder of your app directory.
