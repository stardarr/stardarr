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

```
git clone https://github.com/stardarr/stardarr.git
cd stardarr

docker network create internal_network
docker network create web

cd CloudflareDDNS
cp .env.example .env
~ modify .env ~
docker compose up -d
cd ..

cd Traefik
cp .env.example .env
~ modify .env ~
docker compose up -d
cd ..

cd <Every Other Service>
cp .env.example .env
~ modify .env ~
docker compose up -d
cd ..
```
