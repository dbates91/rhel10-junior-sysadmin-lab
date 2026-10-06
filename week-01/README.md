# Week 1 — Terminal and Filesystem Foundations

## Goal

Build command-line fluency with the core filesystem operations used constantly in Linux administration.

## Commands Introduced

```text
pwd
ls
ls -l
ls -a
cd
mkdir
touch
cp
mv
rm
rmdir
```

Commands are not practiced as isolated trivia. Each command is introduced through a small simulated work task.

## Lab Progression

### Lab 1.1 — Prepare an Application Workspace

**Status:** Ready to begin

Scenario: A new internal application needs directories for configuration files, logs, backups, and temporary data.

Skills:

- Identify the current working directory
- Inspect directory contents
- Create directories
- Create files
- Navigate between directories
- Verify the final state

### Lab 1.2 — Back Up a Configuration File

Scenario: Create a backup of an application configuration file before a change.

Primary new command:

```bash
cp
```

### Lab 1.3 — Move and Rename Files

Scenario: Correct files that were placed in the wrong location and rename files according to an operational standard.

Primary new command:

```bash
mv
```

### Lab 1.4 — Remove Obsolete Files Safely

Scenario: Inspect and remove obsolete temporary files without deleting the wrong data.

Primary new command:

```bash
rm
```

### Week 1 Ticket

After the guided labs, a reduced-hint ticket will require the same skills without providing the commands.

## Administrative Habit

The Week 1 workflow is:

```text
Establish location
        ↓
Inspect existing state
        ↓
Make the requested change
        ↓
Verify the change
```

This pattern will remain part of every later lab.
