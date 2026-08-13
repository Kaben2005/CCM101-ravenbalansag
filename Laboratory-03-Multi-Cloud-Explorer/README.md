# Linux System Investigation & Cloud Mapping

This investigation explores system hardware and operating system parameters using a **Killercoda Ubuntu Playground** environment and maps those specifications to equivalent cloud hosting services across AWS, Azure, and GCP.

---

## 1. Collected System Specifications

Based on terminal commands executed in the Killercoda environment:

### Operating System Information (`cat /etc/os-release`)
* **OS Name:** Ubuntu 24.04.4 LTS (Noble Numbat)
* **Architecture / ID:** `ubuntu` (Debian-based)
* **Version ID:** `24.04`

### CPU Information (`lscpu`)
* **Architecture:** `x86_64` (64-bit)
* **CPU Count:** 1 vCPU
* **CPU Model:** Intel Xeon E312xx (Sandy Bridge, IBRS update) @ 2.0GHz
* **Virtualization:** KVM (Full Virtualization)

### Memory / RAM Information (`free -h`)
* **Total Memory:** ~2.0 GiB (1.9 GiB usable)
* **Used Memory:** 411 MiB
* **Available Memory:** 1.5 GiB
* **Swap Space:** 1.0 GiB

### Disk Space Information (`df -h`)
* **Root Filesystem (`/`):** ~30 GiB Total Size (Standard Killercoda container/VM allocation)

---

## 2. System Investigation Summary Table

| Parameter | Observed Terminal Output |
| :--- | :--- |
| **Operating System** | Ubuntu 24.04.4 LTS (Noble Numbat) |
| **CPU Specs** | 1 vCPU (Intel Xeon E312xx @ 2.0GHz, x86_64) |
| **RAM (Memory)** | 1.9 GiB (~2.0 GB) |
| **Swap Space** | 1.0 GiB |
| **Storage Allocation** | ~30 GB Root Partition |
| **Primary Hypervisor** | KVM |

---

## 3. Cloud Provider Migration Mapping

If this Killercoda Linux server (Ubuntu 24.04 LTS, 1 vCPU, 2 GB RAM, 30 GB Disk) were migrated to the cloud, the corresponding virtual machine compute instances and block storage services across AWS, Azure, and GCP would be:

| Cloud Platform | Compute Service | Equivalent Instance Size | Storage Service |
| :--- | :--- | :--- | :--- |
| **Amazon Web Services (AWS)** | **Amazon EC2** | `t3.small` (2 vCPUs, 2 GiB RAM) or `t3.micro` (2 vCPUs, 1 GiB RAM) | 30 GB EBS General Purpose SSD (`gp3`) |
| **Microsoft Azure** | **Azure Virtual Machines** | `Standard_B1ms` (1 vCPU, 2 GiB RAM) | 30 GB Premium SSD / Standard SSD Managed Disk |
| **Google Cloud Platform (GCP)** | **Compute Engine** | `e2-small` (2 vCPUs, 2 GiB RAM) | 30 GB Standard / Balanced Persistent Disk |

---

## 4. Migration Justification & Cloud Service Analysis

### Amazon Web Services (AWS)
* **Compute Choice:** **Amazon EC2 `t3.small`**. Provides 2 GiB of RAM to comfortably fit the 1.9 GiB system allocation on general-purpose burstable compute.
* **Storage Choice:** **Amazon EBS `gp3`**. A 30 GB volume attached as the root drive provides predictable baseline IOPS and throughput.
* **OS Compatibility:** AWS natively supports Canonical Ubuntu 24.04 LTS via official Amazon Machine Images (AMIs).

### Microsoft Azure
* **Compute Choice:** **Azure VM `Standard_B1ms`**. Provides 1 vCPU and 2 GiB RAM, making it an exact match for lightweight Linux workloads and web utilities.
* **Storage Choice:** **Azure Premium SSD Managed Disk (30 GB)**. Offers fast boot times and consistent disk performance for the OS.
* **OS Compatibility:** Azure Marketplace fully supports Ubuntu 24.04 LTS server deployment out of the box.

### Google Cloud Platform (GCP)
* **Compute Choice:** **Google Compute Engine `e2-small`**. Features 2 GiB RAM and 0.5–2 vCPUs on shared infrastructure, providing a cost-effective hosting option.
* **Storage Choice:** **GCP Balanced Persistent Disk (30 GB)**. Cost-efficient boot disk option tailored for lightweight Linux virtual machines.
* **OS Compatibility:** GCP natively supports official Ubuntu 24.04 LTS boot images via its public image family.
