# Laboratory 01: Welcome to the Cloud

## Mission Overview
The objective of this laboratory activity is to explore a remote Linux environment using KillerCoda, set up a dedicated user workspace, investigate system specs, and build a structured Cloud Computing portfolio on GitHub.

## Objectives
- Launch and verify an Ubuntu Linux playground environment.
- Create a new user with custom privileges and home directory.
- Inspect system hardware and operating system details.
- Build a structured workspace directory.
- Document lab progress and push findings to a GitHub repository.

## Activities Performed
1. **Cloud Environment Access:** Launched an Ubuntu 24.04 instance on KillerCoda.
2. **User Management:** Created the user account `ravenbalansag` with `sudo` permissions and set up its home directory.
3. **Environment Investigation:** Gathered distribution info, kernel version, CPU details, memory size, and available disk space using CLI tools.
4. **Workspace Construction:** Organized workspace directories (`Notes`, `Reports`, `Screenshots`, `ravenbalansag`).
5. **Documentation & Version Control:** Created Markdown documentation files and committed them to GitHub.

## Linux Commands Used
- `sudo useradd` / `sudo passwd` / `sudo usermod` – Managing user accounts and permissions.
- `su -` – Switching user sessions.
- `cat /etc/os-release` – Checking the OS distribution details.
- `uname -r` – Checking the Linux kernel version.
- `lscpu` – Inspecting CPU information.
- `free -h` – Checking system RAM utilization.
- `df -h` – Inspecting disk storage availability.
- `mkdir -p` – Creating directory structures.
- `mv` – Moving and renaming files or directories.
- `nano` / `cat` – Creating, editing, and reading file contents.

## Skills Learned
- Basic user administration and user privilege management in Linux.
- Navigating and querying Linux system metrics via the command line interface (CLI).
- File system navigation and directory management.
- Writing structured technical documentation using Markdown.
- Managing code and project structure using Git and GitHub.
