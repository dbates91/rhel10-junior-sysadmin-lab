# RHEL 10 Junior Linux System Administrator Lab

Hands-on RHEL 10 lab documenting my progression toward RHCSA and Junior Linux System Administrator job readiness.

## Project Purpose

This repository documents my practical Linux administration training in Red Hat Enterprise Linux 10. The goal is to build job-ready junior system administration skills through guided labs, repetition, troubleshooting, and progressively more independent simulated work tasks.

The project is intentionally focused on **doing the work**, not just memorizing commands.

## Lab Environment

### Primary Server: `servera`

- Red Hat Enterprise Linux 10
- VMware Fusion
- Apple Silicon / ARM64
- 4 vCPU
- 4 GB RAM
- 40 GB virtual disk
- NAT networking
- Terminal-first / headless administration environment
- Red Hat repositories registered
- `open-vm-tools` installed and active

`servera` is kept as the primary administration system so the labs reflect realistic Linux server work.

### Desktop Learning Environment

A full clone of `servera` was created and configured with GNOME.

The desktop clone is used to:

- Learn RHEL as an operating system
- Visually inspect filesystem and system changes
- Reinforce the relationship between terminal commands and system state
- Explore GUI tools without changing the primary server lab

Administrative work is still performed from the terminal first.

## Training Method

Each topic follows this progression:

**Understand → Guided Build → Repeat → Reduced Hints → Break/Fix → Blind Ticket → Verify → Explain → Document**

As the course progresses, the labs become less command-driven and more like actual junior Linux administrator tickets.

## 12-Week Training Roadmap

| Week | Focus |
|---|---|
| 1 | Terminal, filesystem navigation, files, directories, paths |
| 2 | Text processing, search, redirection, archives, Vim |
| 3 | Users, groups, permissions, ACLs, sudo |
| 4 | Processes, systemd, services, logs |
| 5 | Networking, DNS, hostnames, SSH |
| 6 | firewalld and SELinux |
| 7 | Disks, partitions, filesystems, mounts, swap |
| 8 | LVM, NFS, autofs |
| 9 | Packages, repositories, patching |
| 10 | Bash, scheduling, time, basic performance |
| 11 | Boot recovery and mixed break/fix troubleshooting |
| 12 | Junior SysAdmin job simulation and RHCSA-style performance work |

## Repository Structure

```text
.
├── README.md
├── setup/
│   ├── rhel10-vmware-installation.md
│   ├── post-install-validation.md
│   └── lab-environment.md
├── week-01/
│   └── README.md
├── troubleshooting/
│   └── README.md
├── scripts/
│   └── README.md
└── screenshots/
    └── README.md
```

## Skills This Project Will Demonstrate

By the end of the project, this repository will show practical experience with:

- RHEL command-line administration
- Filesystem navigation and file management
- User and group administration
- Linux permissions and ACLs
- systemd and service management
- Log analysis
- Network configuration and troubleshooting
- SSH
- firewalld
- SELinux
- Storage and LVM
- NFS and autofs
- Package and repository management
- Bash scripting
- Scheduled jobs
- Boot and recovery tasks
- Troubleshooting and ticket documentation

## Current Status

Environment setup is complete. Week 1 labs are beginning with Linux filesystem fundamentals and simulated junior administrator tasks.
