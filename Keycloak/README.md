# Keycloak Setup

Source: [Docs](https://www.keycloak.org/getting-started/getting-started-zip),  [Keycloak and traefik in docker swarm](https://geek-cookbook.funkypenguin.co.nz/recipes/keycloak/)
Start with downloading the [latest stable release](https://github.com/keycloak/keycloak/releases).
At the time of writing this, its [Keycloak-23.0.7](keycloak-23.0.7.zip)
Extract the file, then enter the dir.

Then run
```bash
bin/kc.sh start-dev
```
This should start the app up on port 8080.

[https://geek-cookbook.funkypenguin.co.nz/docker-swarm/traefik-forward-auth/keycloak/](https://geek-cookbook.funkypenguin.co.nz/docker-swarm/traefik-forward-auth/keycloak/)

### [Proxy Mode](https://www.keycloak.org/server/reverseproxy)

## [Database](https://www.keycloak.org/server/db)
