# Homelab

My personal homelab and portfolio project for hands-on experience with networking, infrastructure, virtualization, Linux, containers, monitoring, and cybersecurity.

### Technologies

[![Proxmox](https://img.shields.io/badge/Proxmox-E57000?logo=proxmox&logoColor=white)](https://www.proxmox.com/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)](https://www.docker.com/)
[![Linux](https://img.shields.io/badge/Linux-FCC624?logo=linux&logoColor=black)](https://www.linux.org/)
[![Debian](https://img.shields.io/badge/Debian-A81D33?logo=debian&logoColor=white)](https://www.debian.org/)
[![Tailscale](https://img.shields.io/badge/Tailscale-242424?logo=tailscale&logoColor=white)](https://tailscale.com/)
[![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?logo=cloudflare&logoColor=white)](https://www.cloudflare.com/)

### Project Status

![Status](https://img.shields.io/badge/Status-Work%20in%20Progress-yellow)

This repository serves as the central hub for documenting my homelab and its ongoing development while helping me gain practical experience beyond the classroom in IT, networking, systems administration, and cybersecurity.

### OPNsense Network Segmentation

Deployment in progress. The homelab is being migrated behind OPNsense with dedicated VLANs for server and management traffic, managed switch trunking, and updated routing and firewall policies.

Final documentation will be added once the migration and validation process is complete.

---

## Architecture

Current environment:

`Home Network → Managed Switch → Proxmox Hosts → LXC / Docker → Self-Hosted Services`

Remote administration and access are handled primarily through **Tailscale**.

---

## Documentation

### Getting Started
- [Homelab Overview](docs/getting-started/overview.md)
- [Goals](docs/getting-started/goals.md)

### Infrastructure
- [Hardware](docs/hardware/)
- [Networking](docs/networking/)
- [Virtualization](docs/virtualization/)

### Operations
- [Monitoring](docs/monitoring/)
- [Security](docs/security/)
- [Troubleshooting](docs/troubleshooting/)

### Services
- [Service Documentation](docs/services/)

---

## Main Services

| Service | Purpose | Documentation |
| --- | --- | --- |
| **Pi-hole** | DNS filtering and network-wide ad blocking | [View Docs](docs/services/pihole.md) |
| **Nginx Proxy Manager** | Reverse proxy and HTTPS management | [View Docs](docs/services/nginx-proxy-manager.md) |
| **Uptime Kuma** | Service and infrastructure monitoring | [View Docs](docs/services/uptime-kuma.md) |
| **Homarr** | Central dashboard for homelab services | [View Docs](docs/services/homarr.md) |
| **Jellyfin** | Self-hosted media server | [View Docs](docs/services/jellyfin.md) |
| **NetBox** | Network and infrastructure documentation | [View Docs](docs/services/netbox.md) |

**[View all service documentation →](docs/services/)**

---

## Repository Resources

- [All Documentation](docs/)
- [Network Diagrams](diagrams/)
- [Screenshots](screenshots/)
- [Sanitized Configurations](configs/)
- [Scripts](scripts/)

---

## Future Plans

The homelab continues to evolve as I experiment with new technologies and improve the existing infrastructure.

Planned areas of development include:

- Improve network segmentation and VLAN design
- Expand monitoring and observability
- Build out the Proxmox cluster
- Expand self-hosted services
- Improve backup, recovery, redundancy, and infrastructure reliability

**[View current homelab goals →](docs/getting-started/goals.md)**

> A dedicated roadmap will be added as the homelab continues to grow.

---

## Security

Sensitive information such as passwords, API keys, tokens, private keys, and credentials is not intentionally stored in this repository.

Configurations published here are sanitized before being committed.
