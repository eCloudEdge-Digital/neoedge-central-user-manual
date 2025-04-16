# NeoEdge Central
NeoEdge Central is a cloud-based management platform allows you to easily manage, configure, and deploy IoT applications on remote gateways.

For more information, please visit [NeoEdge Central homepage](https://www.ecloudedge.com/).

## Table of Contents
- [Installation](#installation)
    - [Prerequisites](#prerequisites)
    - [Steps](#steps)
- [Usage](#usage)
    - [Basic Usage](#basic-usage)
    - [Examples](#examples)


## Installation

### Prerequisites

* **OS requirements:**
This software is primarily supported on **Linux (amd64 architecture)**.
    - This software has been tested and is recommended for optimal stability and reliability on **Ubuntu 20.04 LTS** and **Ubuntu 22.04 LTS**.
    - You can verify your OS version by opening a terminal and running the following command.

    ```bash
    lsb_release -a
    ```

* **System requirements:**
This software has been tested and is recommended for

| Component  | Minimum Requirement | 
| --------   | -------- | 
| CPU        | 2 cores| 
| RAM        | 3 GB   | 
| Disk       | 30 GB  | 

* **Docker& Docker Compose:** 
Before you can run this application, you need to ensure you have **Docker Engine and Docker Compose** installed. 
    - You can find installation instructions for your operating system on the official Docker website: [https://docs.docker.com/engine/install/](https://docs.docker.com/engine/install/).
    - This software has been tested and is recommended for optimal stability and reliability on **Docker Engine Version 28.0.4** and **Docker Compose Version v2.34.0**.
    - You can verify that Docker and Docker Compose version by running the following commands in your terminal.

    - Before Docker 20.10 (and Docker Compose V1):
    ```bash
    docker --version
    docker-compose version
    ```
    - With Docker 20.10 and later (Docker Compose V2):
    ```bash
    docker --version
    docker compose version
    ```
### Steps
1.  **Unpack installer.tar.gz into installer folder**
    ```bash
    sudo tar xfvz installer.tar.gz
    ```
2. **Run the installer-linux-amd64 executable**

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
## Usage

### Basic Usage
1.  **Enter the website URL**

After the installation is complete, please visit the NeoEdge Central login page at: https://neoedge-central-domain/login

![Website Screenshot](https://github.com/eCloudEdge-Digital/neoedge-central-user-manual/raw/dev/readme-images/login.png)
    
2. **Log in with the default user**

Please login with the default user
- deafult user account: aiot@ecloudedge.com
- password of the default user: A!oT@6689

### Examples

For more information, please visit 
- [NeoEdge Central Quick Start (English)](https://www.youtube.com/playlist?list=PLUAJDbJOOHqx2JrZCZpMZT_nlDE_qKT2h).
- [NeoEdge Central Quick Start (Chinese)] (https://www.youtube.com/watch?v=rTCuhZzv0oE&list=PLUAJDbJOOHqzpqJ9g9IN0j4ClaQMbtXE8)