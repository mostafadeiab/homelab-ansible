# Services List

These playbooks set up the follow services:

Homelab Services
Traefik: Acts as the reverse proxy with secure TLS (via Cloudflare) and Authelia for middleware-based authentication. HTTP → HTTPS redirection is configured.

Authelia: Provides authentication for Traefik-routed services.

Code Server: IDE hosted in the browser, accessible through code.{{ domain }}.

Dashdot, Guacamole, Homarr, Monitoring: Dashboard and management tools for your system and services.

Pi-hole: Blocks ads and trackers, improving network privacy.

Portainer: Docker management dashboard.

Vaultwarden: Password management service.

Watchtower: Automatically updates Docker containers on the homelab.

Wireguard: VPN solution to provide secure access to the network.

Ollama & Gogs: Utilize shared storage from the homeserver.

Homeserver Services
MySQL: Database for storage-heavy apps like Nextcloud.

n8n: Workflow automation tool.

Nextcloud: Personal cloud storage and productivity solution.

Syncthing: Synchronizes files across devices.

Filebrowser: Provides access to homeserver files through a web interface.

Unmanic: Media file optimizer.