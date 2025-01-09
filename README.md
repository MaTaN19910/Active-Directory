# Active-Directory
Overview

Active Directory (AD) is a directory service developed by Microsoft that enables administrators to manage permissions, access, and resources within a network. It is a critical component of enterprise IT environments, offering centralized authentication, authorization, and directory services.
This repository provides an automated setup for:

Deploying a Microsoft Certification Authority (CA) and IIS (Internet Information Services) on a Windows Server to generate and serve logs.

Running a Splunk standalone instance on a Docker container deployed on a Linux EC2 instance.

Sending logs from the IIS server to the Splunk instance for monitoring and analysis.

Prerequisites

For Windows Server (CA & IIS):

A Windows Server machine with administrative access.

Active Directory setup with administrative privileges.

Ensure PowerShell is installed and accessible.

For Linux EC2 Instance (Splunk):

An Amazon EC2 instance running a Linux distribution (e.g., Amazon Linux 2, Ubuntu).

Docker and Docker Compose installed on the Linux EC2 instance.

Tools:

Ansible (for configuration management and automation).

PowerShell (for Windows configuration).

project structure:
.
├── ansible
|── linux
│   ├── inventory.ini
│   ├── roles
│      ├── transfer_cert
│      │   ├── tasks
│      │
│      ├── install_docker
│      │   ├── tasks
|      |
│      ├── install_splunk_standalone
│      │   ├── tasks
│      │   ├── templates
│      │   └── files
|      |
│      |
├── windows
│   ├── roles
│   │   ├── install_iis
│   │   │   ├── files
│   │   │   └── tasks
│   │   └── ca
│   │   |    ├── tasks
│   │   |    └── templates
│   │   └── export_cert
│   │   |    ├── tasks
│   │   └── install_iis
│   │       ├── files
│   │       └── tasks
|
├── README.md