# Homelab

![Homelab](https://img.shields.io/badge/Homelab-KVM%2FQEMU-blue)
![Ubuntu](https://img.shields.io/badge/Ubuntu-24.04-orange)

## Overview
Local virtualization lab built with KVM/QEMU on Ubuntu to practice
server administration and infrastructure management.

## Architecture
- Host machine running KVM/QEMU hypervisor
- Ubuntu Server VM (20GB disk, 4GB RAM, 2 vCPUs)
- Prometheus monitoring on port 9090
- SSH access via port 22

## Setup
- Host: Ubuntu 24.04, Ryzen 7800X3D, 32GB RAM
- Hypervisor: KVM/QEMU with virt-manager
- VM: Ubuntu Server 24.04 LTS

## What's Running
- Ubuntu Server VM with Prometheus monitoring
- SSH access configured
- Network configuration via Netplan

## What I Learned
- Setting up KVM/QEMU hypervisor on Linux
- Creating and configuring VMs
- Network configuration with Netplan
- SSH server setup
- Prometheus monitoring installation

## Next Steps
- Add Windows Server VM
- Configure Azure CLI integration
- Set up monitoring dashboard
- Configure network between multiple VMs