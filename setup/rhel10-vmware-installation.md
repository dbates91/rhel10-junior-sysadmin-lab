# RHEL 10 VMware Fusion Installation

## Objective

Build a clean Red Hat Enterprise Linux 10 virtual machine that can be used as the primary environment for Junior Linux System Administrator and RHCSA training.

## Platform

- Hypervisor: VMware Fusion
- Host architecture: Apple Silicon
- Guest architecture: ARM64 / aarch64
- Operating system: Red Hat Enterprise Linux 10

## Virtual Machine Configuration

The primary lab server is named:

```text
servera
```

Baseline resources:

- 4 vCPU
- 4 GB RAM
- 40 GB virtual disk
- 1 NAT network adapter
- Automatic partitioning for the initial operating system disk

The first installation was intentionally kept simple. Additional virtual disks will be added later when the course reaches partitions, filesystems, LVM, and storage administration.

## Installation Decisions

### Server-first installation

The primary VM was installed as a server rather than relying on a graphical desktop.

This keeps `servera` representative of a Linux server that would normally be administered through a terminal or SSH session.

### Networking

DHCP is used during the early labs.

Static addressing and NetworkManager configuration will be introduced later when networking becomes part of the course.

### Administrative access

A normal administrative user was created with sudo access.

The goal is to perform routine administration through the normal user account and elevate privileges only when required.

## Post-install setup

After installation, the system was registered with Red Hat and the available software repositories were verified.

The system was then updated and VMware guest integration was installed:

```bash
sudo dnf update -y
sudo dnf install -y open-vm-tools
sudo systemctl enable --now vmtoolsd
```

## Desktop Clone

A full clone of `servera` was created for desktop learning.

GNOME was installed on the clone with:

```bash
sudo dnf group install "Server with GUI" -y
sudo systemctl set-default graphical.target
sudo reboot
```

This preserves the original headless server while providing a separate RHEL desktop environment for visual learning and operating-system exploration.

## Design Decision

The project uses two environments for different purposes:

```text
servera
└── Primary headless administration server

rhel10-desktop
└── Full clone with GNOME for visual OS learning
```

The terminal remains the primary administration interface.
