# NeoEdge Central
Integrates OT/IT technologies to enable users to efficiently deploy and manage containerized and edge applications. Whether it's a single site or thousands of edge nodes distributed globally, it provides unified control and real-time updates. This helps enterprises achieve digital transformation with ease, even in large-scale distributed environments.

For more information, please visit [NeoEdge Central homepage](https://www.ecloudedge.com/).

## Table of Contents
- [Installation](#installation)
    - [Prerequisites](#prerequisites)
    - [Installation Steps](#installation-steps)
    - [Uninstallation Steps](#uninstallation-steps)
- [Getting Started](#getting-started)
    - [Basic Usage](#basic-usage)
    - [Further Exploration](#further-exploration)


## Installation

### Prerequisites
Before proceeding with the installation, ensure your system meets the following requirements.
* **OS Requirements:**
NeoEdge Central is primarily supported on **Linux (amd64 architecture)**.
    - For optimal stability and reliability, we highly recommend using **Ubuntu 20.04 LTS** and **Ubuntu 22.04 LTS**.
    
    - To verify your OS version, execute the following terminal command:
    ```bash
    lsb_release -a
    ```

* **System Requirements:**
The following minimum system specifications are recommended for smooth operation:

    | Component  | Minimum Requirement | 
    | --------   | -------- | 
    | CPU        | 4 cores (Intel XeonCPU E5-2673 v3 @ 2.40GHz)| 
    | RAM        | 16 GB   | 
    | Disk       | 32GB SSD  | 

* **Docker& Docker Compose:** 
Before installing NeoEdge Central, ensure you have **Docker Engine and Docker Compose** installed. 
    - Detailed installation instructions for your specific operating system can be found on the [official Docker website](https://docs.docker.com/engine/install/).
    - For optimal stability and reliability, we highly recommend using **Docker Engine Version 28.1.1** and **Docker Compose Version v2.35.1**.
    - You can verify that Docker and Docker Compose version running the following terminal commands.

    - For Docker versions prior to 20.10 (Docker Compose V1):
    ```bash
    docker --version
    docker-compose version
    ```
    - For Docker version 20.10 and later (Docker Compose V2):
    ```bash
    docker --version
    docker compose version
    ```
### Installation Steps
1.  **Extract the Installer:**
    Unpack the installer.tar.gz archive into a dedicated installer directory using the following command:

    ```bash
    sudo tar xfvz installer.tar.gz
    ```
2. **Execute the Installer:**
   Navigate into the newly created installer directory and run the installer-linux-amd64 executable. The estimated installation time is approximately 10 minutes:
   ```bash
   cd installer
   sudo ./installer-linux-amd64 -domain <domain> 
   ```
   ```text
   Available command line options 
   -h
    Help
   -domain
    Required. NeoEdge Central application's domain name, specified as either the IP address of the installed machine or a resolvable DNS domain name associated with it.
   -loglevel
    Optional (default "error").Log level including error, warn, info, debug. 
   -mode
    Optional (default "cli"). Mode to run the installer,including tui (text-based user interface) or cli (command-line interface). 
   ```
3. **Verify Successful Installation:**
   You can confirm that NeoEdge Central has been installed successfully by checking for a specific message in either the installer.log file or the standard output displayed during the installation process. Look for the following confirmation:
   ```bash
   #standard output 
   Installation completed successfully.

   #installer.log message
   {"time":"*","level":"INFO","msg":"Installation completed successfully."}
   ```
  
### Uninstallation Steps  
1.  **Uninstall (TBA):**

## Getting Started
Once the installation is complete, you can access and begin using NeoEdge Central.

### Basic Usage
1. **Accessing NeoEdge Central:**
Open your web browser and navigate to the NeoEdge Central login page using the domain name you specified during installation : 
```bash
https://<neoedge-central-domain>/login
```
![Website Screenshot](https://github.com/eCloudEdge-Digital/neoedge-central-user-manual/raw/dev/readme-images/login.png)
    
2. **Initial Login:**
Log in using the default credentials
- Default Username: aiot@ecloudedge.com
- Default Password: A!oT@6689

### Further Exploration

For more in-depth information and practical demonstrations, please refer to the following resources:
- [NeoEdge Central Quick Start (English)](https://www.youtube.com/playlist?list=PLUAJDbJOOHqx2JrZCZpMZT_nlDE_qKT2h).
- [NeoEdge Central Quick Start (Chinese)](https://www.youtube.com/playlist?list=PLUAJDbJOOHqzpqJ9g9IN0j4ClaQMbtXE8)
