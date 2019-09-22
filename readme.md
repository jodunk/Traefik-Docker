# Howto Use Traefik 1.7.16 - to a Reverse Proxy for Docker

## STEP1. Create Custom Docker Network

`docker network ls`

`docker network create proxy`

`docker network ls`

## STEP2. Create Encrypt Password
Now run the `htpasswd` command to generate a password for traefik dashboard authen.

`htpasswd -nb admin password`

Keep the result in your note.

`admin:$apr1$hEgpZUN2$OYG3KwpzI3T1FqIg9LIbi.`

## STEP3. Create traefik configuration.
Create a new directory 'traefik' for traefik configurae.

`mkdir -p traefik/`

`cd traefik/`

Create Traefik Configuration

`nano traefik.toml`

## STEP3. Create `docker-compose.yml` script.
`nano docker-compose.yml`

Build the container using docker compose command below.

`docker-compose up -d`
