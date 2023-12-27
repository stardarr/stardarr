# Stardarr

A Dockerized Homelab starter kit for you to modify and extend.

Documentation and getting started guide for this repo can be found at [stardarr.dev](https://stardarr.dev).

The majority of the images used in this project are built and hosted by [linuxserver.io](https://www.linuxserver.io/). Documentation about the images can be found at [docs.linuxserver.io](https://docs.linuxserver.io/)

Documentation for each individual service can be found at their respective home pages linked below.

## Services

- [Traefik](https://traefik.io/traefik/)
- [Cloudflare Dynamic DNS](https://github.com/oznu/docker-cloudflare-ddns)
- [Plex](https://www.plex.tv/)
- [Overseer](https://overseerr.dev/)
- [Unmanic](https://docs.unmanic.app/)
- [Nextcloud](https://nextcloud.com/)
- [Fireshare](https://github.com/ShaneIsrael/fireshare)
- [Home Assistant](https://www.home-assistant.io/)
- [NZBGet](https://nzbget.net/)
- [Homarr](https://homarr.dev/)
- [Sonarr](https://sonarr.tv/)
- [Radarr](https://radarr.video/)
- [Readarr](https://readarr.com/)
- [Bazarr](https://www.bazarr.media/)

## Quickstart

Setup Cloudflare then:

```bash
# Clone the repo
git clone https://github.com/stardarr/stardarr.git
cd stardarr

# Create the Docker Networks
docker network create internal_network
docker network create web

cd CloudflareDDNS
cp .env.example .env # Copy the example environment file
nano .env # Customize your configuration
docker compose up -d # Start the service
cd ..

cd Traefik
cp .env.example .env # Copy the example environment file
nano .env # Customize your configuration
docker compose up -d # Start the service
cd ..

cd <Every Other Service>
cp .env.example .env # Copy the example environment file
nano .env # Customize your configuration
docker compose up -d # Start the service
cd ..
```

# Service URLs

| Service        | URL                  | Proxied |
| -------------- | -------------------- | ------- |
| Plex           | plex.domain.com      | Yes     |
| Overseerr      | overseerr.domain.com | Yes     |
| Nextcloud      | cloud.domain.com     | Yes     |
| Fireshare      | videos.domain.com    | Yes     |
| Home Assistant | localhost:8123       | no      |
| SABnzbd        | localhost:8080       | no      |
| Unmanic        | localhost:8888       | no      |
| Homarr         | localhost:7575       | no      |
| Sonarr         | localhost:8989       | no      |
| Radarr         | localhost:7878       | no      |
| Readarr        | localhost:8787       | no      |
| Bazarr         | localhost:6767       | no      |
