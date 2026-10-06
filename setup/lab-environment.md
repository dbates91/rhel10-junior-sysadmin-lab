# Lab Environment Design

## Objective

Maintain separate environments for server administration practice and desktop operating-system learning.

## Environment 1: servera

`servera` is the primary system used throughout the Junior Linux System Administrator course.

### Purpose

- Terminal-first Linux administration
- RHCSA-style practice
- System configuration
- Troubleshooting
- Break/fix exercises
- Simulated work tickets

### Operating model

The system remains headless so administration habits are built around the shell rather than graphical tools.

## Environment 2: rhel10-desktop

`rhel10-desktop` is a full clone of `servera` with GNOME installed.

### Purpose

- Learn the RHEL desktop environment
- Explore Linux as a complete operating system
- Visually inspect filesystem changes
- Compare GUI state with terminal output

## Learning Rule

The terminal is used first.

For example:

```bash
mkdir ~/Projects
```

Afterward, GNOME Files can be opened to visually verify that the `Projects` directory now exists.

The GUI is used as a learning aid and verification tool rather than a substitute for command-line administration.

## Why Two VMs?

Keeping the environments separate prevents the desktop packages and GUI configuration from changing the character of the primary server lab.

It also makes it possible to practice realistic server administration while still building familiarity with Linux as an everyday operating system.
