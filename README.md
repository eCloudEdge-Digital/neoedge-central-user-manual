English | [繁體中文](./README-CN.md) 
# NeoEdge Central
NeoEdge Central is a cloud-based management platform allows you to easily manage, configure, and deploy IoT applications on remote gateways.

For more information, please visit [NeoEdge Central homepage](https://www.ecloudvalley.com/neoedge-en/p/NeoEdgeCentral).

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
This software is primarily tested and supported on **Linux (amd64 architecture)**.


* **Docker& Docker Compose:** 
Before you can run this application, you need to ensure you have **Docker Engine and Docker Compose** installed. 
    - You can find installation instructions for your operating system on the official Docker website: [https://docs.docker.com/engine/install/](https://docs.docker.com/engine/install/).
    - You can verify that Docker and Docker Compose are installed correctly by running the following commands in your terminal.

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
    Required. NeoEdge Central application's ip address or domain name.
   -loglevel
    Optional (default "error").Log level including error, warn, info, debug. 
   -mode
    Optional (default "cli"). Mode to run the installer,including tui or cli. 
   ```
## Usage

### Basic Usage
1.  **Enter the website URL**

After the installation is complete, please visit the NeoEdge Central login page at: https://neoedge-central-domain/login

![Website Screenshot](https://github.com/eCloudEdge-Digital/neoedge-central-user-manual/raw/dev/readme-images/login.png)
    
2. **Log in with the default user**

Please login with the default 
- deafult user: aiot@ecloudedge.com
- password of the default user: A!oT@6689


