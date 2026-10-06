# Post-Installation Validation

## Objective

Confirm that the RHEL 10 virtual machine is healthy and ready for administration labs before making training changes.

## Validation Commands

### Identify the system

```bash
hostnamectl
cat /etc/redhat-release
uname -m
```

These commands confirm the hostname, RHEL release, and system architecture.

### Check networking

```bash
ip -br addr
```

This provides a concise view of network interfaces and assigned IP addresses.

### Check storage

```bash
df -h
```

This confirms mounted filesystems and current disk usage.

### Check memory

```bash
free -h
```

This confirms the VM can see the expected memory allocation.

### Confirm administrative access

```bash
sudo whoami
```

Expected result:

```text
root
```

This verifies that the normal administrative account can elevate privileges through sudo.

### Verify VMware Tools

```bash
systemctl is-active vmtoolsd
```

Expected result:

```text
active
```

### Verify Red Hat repositories

```bash
sudo dnf repolist
```

This confirms that package repositories are available before package-management labs begin.

## Snapshot Strategy

A clean baseline snapshot should be maintained before destructive labs.

Suggested snapshot name:

```text
servera-clean-baseline
```

Purpose:

- Return to a known-good RHEL state
- Recover from destructive lab mistakes
- Allow troubleshooting practice without fear of permanently damaging the environment

Snapshots are a lab safety mechanism, not a replacement for learning how to troubleshoot and recover Linux systems.
