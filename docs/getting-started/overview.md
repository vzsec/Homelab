# Homelab Overview

My homelab is a personal infrastructure environment built to gain hands-on experience with networking, virtualization, Linux, containers, monitoring, systems administration, and cybersecurity.

The environment gives me a place to deploy real services, experiment with new technologies, troubleshoot problems, and apply concepts beyond the classroom while continuing to develop practical IT and infrastructure skills.

---

## Environment Overview

The homelab consists of multiple physical systems running **Proxmox VE**, managed networking equipment, and a growing collection of self-hosted infrastructure and application services.

The primary Proxmox infrastructure includes a main server alongside two **Lenovo ThinkCentre** nodes. These systems provide the compute resources used to run virtualized infrastructure and self-hosted services.

Workloads are primarily deployed using **LXC containers** and **Docker**, allowing services to remain separated while efficiently using the available hardware.

The environment currently includes:

- Multiple Proxmox hosts
- Lenovo ThinkCentre compute nodes
- Managed Ethernet switching
- LXC and Docker workloads
- Internal DNS and filtering
- Infrastructure and service monitoring
- Secure remote administration
- Self-hosted applications and media services

A dedicated **OPNsense** firewall appliance is also being developed for future routing, firewalling, and network segmentation within the homelab.

Detailed hardware specifications and individual systems are documented separately.

**[View hardware documentation →](../hardware/)**

---

## Architecture

The current environment operates within the existing home network, with the managed switch providing connectivity to the physical homelab infrastructure.

```text
Internet
   │
   ▼
Home Network
   │
   ▼
Managed Switch
   │
   ▼
Proxmox Infrastructure
   │
   ▼
LXC / Docker
   │
   ▼
Self-Hosted Services
```

The architecture is designed to remain modular so individual parts of the environment can be changed, expanded, or migrated as the homelab develops.

Future network development will introduce dedicated routing and segmentation for the homelab while keeping the primary home network separate.

A more detailed topology showing physical systems, network connections, and infrastructure relationships is maintained separately.

**[View network diagrams →](../../diagrams/)**

---

## Network Design

The current homelab infrastructure operates on the existing home network while managed switching provides physical connectivity between systems.

**Pi-hole** provides internal DNS and network-wide filtering, while **Tailscale** provides secure remote administration without requiring management services to be directly exposed to the public internet.

A dedicated **OPNsense** firewall appliance has been configured and tested as part of the continued development of the network. Future deployment plans include moving the homelab behind OPNsense and introducing greater separation between the home network and lab infrastructure.

Current networking features include:

- Managed Ethernet switching
- Internal DNS and filtering through Pi-hole
- Secure remote administration through Tailscale
- Limiting unnecessary exposure to the public internet

Planned network improvements include:

- Separating homelab infrastructure from the primary home network
- VLAN-based network segmentation
- Dedicated server and management networks
- Firewall rules controlling communication between network segments
- OPNsense routing and firewalling for the homelab

These improvements will provide additional opportunities to gain practical experience with routing, switching, VLANs, firewall policies, DNS, network segmentation, and access control as the network evolves.

Detailed IP addressing, VLAN assignments, firewall rules, DNS configuration, and switching configuration are maintained within the networking documentation.

**[View networking documentation →](../networking/)**

---

## Virtualization

**Proxmox VE** serves as the primary virtualization platform for the homelab.

Multiple Proxmox hosts provide the compute layer used to run infrastructure and application workloads. Different virtualization technologies are used depending on the requirements of each workload.

The environment primarily uses:

- **LXC containers** for lightweight Linux infrastructure
- **Docker** for containerized applications and service stacks
- **Virtual machines** when a complete operating system environment or additional isolation is required
- Multiple physical Proxmox hosts for distributing workloads

A future goal of the project is to continue developing the environment into a **Proxmox cluster**, providing experience with multi-node virtualization management and additional infrastructure concepts.

Detailed host configuration, container deployment, storage, and clustering information is documented separately.

**[View virtualization documentation →](../virtualization/)**

---

## Services

The homelab hosts a variety of self-hosted services that support the infrastructure itself while also providing useful applications.

Services are separated into several general categories:

| Category | Examples | Purpose |
| --- | --- | --- |
| **Infrastructure** | Pi-hole, Nginx Proxy Manager | DNS, filtering, reverse proxying, and HTTPS |
| **Monitoring** | Uptime Kuma | Infrastructure and service availability monitoring |
| **Management** | Homarr, NetBox | Service dashboards and infrastructure documentation |
| **Media** | Jellyfin, Jellyseerr | Self-hosted media and request management |
| **Remote Access** | Tailscale | Secure remote administration and connectivity |

Additional supporting services are deployed as needed, and the service environment continues to change as new technologies are tested.

Each major service has its own documentation containing information about its purpose, deployment, configuration, and role within the homelab.

**[View service documentation →](../services/)**

---

## Security

Security is incorporated into the design and operation of the homelab rather than being treated as a separate component.

The environment provides a practical place to apply security concepts while learning how they interact with real infrastructure.

Current practices include:

- Avoiding unnecessary public-facing ports and services
- Using Tailscale for secure remote administration
- Using Pi-hole for DNS filtering
- Using HTTPS and reverse proxying where appropriate
- Limiting access to management interfaces
- Following least-privilege principles where practical
- Keeping credentials, API keys, tokens, and private keys out of GitHub
- Sanitizing configurations before publishing them to the repository

Future security improvements include:

- Network and VLAN segmentation
- Dedicated management and server networks
- Inter-network firewall policies
- Greater isolation between the homelab and primary home network

Security practices will continue to evolve alongside the infrastructure as additional services, networks, and technologies are introduced.

Detailed security architecture, firewall policies, remote access, and hardening practices are documented separately.

**[View security documentation →](../security/)**

---

## Project Philosophy

The purpose of the homelab extends beyond simply hosting applications.

The environment is designed to provide practical experience with the complete lifecycle of operating infrastructure:

**Design → Deploy → Configure → Secure → Monitor → Troubleshoot → Document**

Each part of the project provides an opportunity to understand not only how a technology is configured, but also why it is being used, how it interacts with other infrastructure, and how problems can be identified and resolved.

The homelab also serves as an ongoing portfolio project where infrastructure decisions, configurations, diagrams, troubleshooting experiences, and future improvements can be documented as the environment grows.

The overall goal is to build practical experience with technologies and concepts used in real IT, networking, systems administration, and cybersecurity environments.

---

## Related Documentation

- [Goals](goals.md)
- [Hardware](../hardware/)
- [Networking](../networking/)
- [Virtualization](../virtualization/)
- [Services](../services/)
- [Security](../security/)
- [Monitoring](../monitoring/)
- [Troubleshooting](../troubleshooting/)
- [Network Diagrams](../../diagrams/)
