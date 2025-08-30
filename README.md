# C-Box

## Overview
C-Box a minimal implementation of a Linux container in C, inspired by [Lizzie's blog post](https://blog.lizzie.io/linux-containers-in-500-loc.html). The project demonstrates core container concepts like namespaces, cgroups, and process isolation, built from scratch.

## Features
- Creates an isolated environment using Linux namespaces
- Utilizes cgroups to limit resource usage
- Executes a user-specified command in the containerized environment
- Lightweight and simple, focusing on core container mechanics

## Prerequisites
- Linux system with kernel support for namespaces and cgroups
- GCC or another C compiler
- Root privileges (required for certain namespace and cgroup operations)

## Build Instructions
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/linux-container-c.git
   cd linux-container-c
   ```
2. Compile the code:
   ```bash
   gcc -o container container.c
   ```
3. Run the container (as root):
   ```bash
   sudo ./container /bin/sh
   ```

## Usage
Run the compiled binary with a command to execute inside the container:
```bash
sudo ./container <command>
```
Example:
```bash
sudo ./container /bin/bash
```
This starts a new shell in an isolated environment

## Acknowledgments
- Based on the tutorial by [Lizzie](https://blog.lizzie.io/linux-containers-in-500-loc.html).
