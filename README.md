# 🏠 Homelab

Personal homelab built to gain hands-on experience with virtualization, containers, networking, and server administration — directly supporting my path toward Azure certification (AZ-104) and a career as a Cloud Engineer.

---

## 🚀 Journey

This homelab has evolved over time from a simple virtualization setup on my workstation to a dedicated always-on server running a full self-hosted stack.

```
Phase 1 (2025)         →        Phase 2 (2026)
KVM/QEMU on Ubuntu     →        Proxmox on dedicated hardware
Single VM + Prometheus →        Docker stack with multiple services
```

---

## 🖥️ Hardware

### Phase 1 — Workstation
| Component | Details |
|---|---|
| **OS** | Ubuntu 24.04 |
| **CPU** | AMD Ryzen 7800X3D |
| **RAM** | 32 GB |
| **Hypervisor** | KVM/QEMU with virt-manager |

### Phase 2 — Dedicated Server
| Component | Details |
|---|---|
| **Host** | Dell OptiPlex 3060 |
| **CPU** | Intel Core i3-8100T (4 Cores) |
| **RAM** | 8 GB DDR4 |
| **Storage (OS)** | 256 GB SSD |
| **Storage (Media)** | 4 TB HDD (via USB Docking Station) |
| **Hypervisor** | Proxmox VE 9.1 |

---

## 📝 Setup Log

### Phase 1 — KVM/QEMU (2025)

- Set up KVM/QEMU hypervisor on Ubuntu workstation using virt-manager
- Created Ubuntu Server 24.04 VM (20 GB disk, 4 GB RAM, 2 vCPUs)
- Configured SSH access and networking via Netplan
- Deployed Prometheus monitoring on port 9090
- Practiced server administration and infrastructure management

**What I learned:**
- Setting up a Type 2 hypervisor on Linux
- VM creation and resource management
- Network configuration with Netplan
- SSH server setup
- Basic monitoring with Prometheus

---

### Phase 2 — Proxmox Dedicated Server (2026-04-02)

**Proxmox Installation**
- Purchased Dell OptiPlex 3060 as dedicated homelab server
- Downloaded Proxmox VE 9.1 ISO and flashed USB stick with Rufus (DD mode)
- Installed Proxmox VE — completely replaces Windows, runs 24/7

**Docker VM**
- Created Ubuntu Server 24.04 VM (2 cores, 2 GB RAM, 40 GB disk)
- Installed Docker via official install script
- Deployed Portainer CE for Docker management via Web UI

**Pi-hole**
- Deployed Pi-hole via Docker Compose stack in Portainer
- Resolved port 53 conflict by disabling Ubuntu's `systemd-resolved`
- Initialized blocklist with 91,978 domains
- Set Pi-hole as DNS server in router — all network devices now ad-free

**What I learned:**
- Difference between Type 1 (Proxmox) and Type 2 (KVM) hypervisors
- Docker container management with Portainer
- DNS fundamentals and how Pi-hole intercepts queries
- Debugging port conflicts in Linux
- Docker Compose / stack deployment

---

## 🛠️ Current Stack

| Service | Purpose | Status |
|---|---|---|
| **Proxmox VE 9.1** | Type 1 Hypervisor | ✅ Running |
| **Ubuntu Server 24.04** | Docker host VM | ✅ Running |
| **Docker + Portainer** | Container management | ✅ Running |
| **Pi-hole** | DNS & network ad blocking | ✅ Running |
| **Jellyfin** | Self-hosted media server | 🔜 Planned |
| **Homarr** | Homelab dashboard | 🔜 Planned |
| **Nginx Proxy Manager** | Reverse proxy & SSL | 🔜 Planned |
| **Tailscale** | Remote access VPN | 🔜 Planned |
| **Active Directory** | Windows Server VM | 🔜 Planned |
| **Prometheus + Grafana** | Monitoring stack | 🔜 Planned |

---

## 🎯 Goals

- [x] Set up KVM/QEMU hypervisor on Linux
- [x] Deploy Prometheus monitoring
- [x] Set up dedicated Proxmox server
- [x] Create Docker VM with Portainer
- [x] Deploy Pi-hole as network DNS
- [ ] Deploy Jellyfin media server
- [ ] Set up Homarr dashboard
- [ ] Configure Nginx Proxy Manager with SSL
- [ ] Enable remote access with Tailscale
- [ ] Set up Active Directory VM
- [ ] Add Prometheus + Grafana monitoring

---

## 🔗 Related Projects

- [azure-network-lab](https://github.com/noelqy/azure-network-lab) — Azure VNet/NSG/Peering scripts
