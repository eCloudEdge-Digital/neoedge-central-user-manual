# NeoEdge Central
Integrates OT/IT technologies to enable users to efficiently deploy and manage containerized and edge applications. Whether it's a single site or thousands of edge nodes distributed globally, it provides unified control and real-time updates. This helps enterprises achieve digital transformation with ease, even in large-scale distributed environments.

For more information, please visit [NeoEdge Central homepage](https://www.ecloudedge.com/).

## Table of Contents
- [Installation](#installation)
    - [Prerequisites](#prerequisites)
    - [Installation Steps](#installation-steps)
    - [License Application](#license-application)
    - [Uninstallation Steps](#uninstallation-steps)
- [Getting Started](#getting-started)
    - [Basic Usage](#basic-usage)
    - [Further Exploration](#further-exploration)


## Installation

### Prerequisites
Before proceeding with the installation, ensure your system meets the following requirements.
* **OS Requirements:**
NeoEdge Central is supported on **Linux (amd64 architecture)**.
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
  
* **TPM2.0 Requirements:**
TPM2.0 is mandatory for NeoEdge Central on encrypt and protect essentail data and keys. Please ensure your machine or virtual machine is equipped with TPM2.0.
    - For Azure, please refer to <a href="https://learn.microsoft.com/en-us/azure/virtual-machines/trusted-launch">this doc</a> to enable trused launch on VM.
    - For AWS, please refer to <a href="https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/nitrotpm.html">this doc</a> to enable NitroTPM on EC2.
    - For GCP, please refer to <a href="https://cloud.google.com/compute/shielded-vm/docs/shielded-vm#vtpm">this doc</a> to enable vTPM on GCP VM.

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

4. **Configure Your Firewall:**
   The following firewall policies are mandatory on your NeoEdge Central host:
    
    | Source IP  | Source Port | Destination IP | Destination Port  
    | --------   | -------- | -------- | -------- | 
    | Any or your Browser | Any | ```<neoedge-central-ip>``` | 443 
    | Any or Gateway | Any | ```<neoedge-central-ip>``` | 8443 
    | Any or Gateway | Any | ```<neoedge-central-ip>``` | 8883
    
### License Application 
NeoEdge Central application requires a valid license for use. Please follow these steps to apply: (TBU)

1. **Download License Request File:**
   To apply for a license, you must first dowload a license request file.

<!-- ![License Request](https://github.com/eCloudEdge-Digital/neoedge-central-user-manual/raw/dev/readme-images/license-request.png) -->

<img src="https://github.com/eCloudEdge-Digital/neoedge-central-user-manual/raw/dev/readme-images/license-request.png" alt="License Request" width="50%" height="auto" align="center">

    📣 **Reminder:** 
    * **Use the latest downloaded license request file:** If you've generated the license request file multiple times, please use the most recent version for your application, as each generation creates unique license content.


2. **Start Your License Application:**
    To ensure you receive the correct license, please first decide the number of gateways and advanced apps your deployment requires.

    Once you have this information, please have your downloaded license request file ready and contact your ECE sales representative to start your application.

    If you have any questions or need further clarification, please don't hesitate to contact us at [sales@ecloudedge.com](mailto:sales@ecloudedge.com).

3. **Install NeoEdge Central License:**
    After license is issued, please upload the received license key file to install the license and set up the initial user account and password.

<img src="https://github.com/eCloudEdge-Digital/neoedge-central-user-manual/raw/dev/readme-images/license-upload.png" alt="License Upload" width="50%" height="auto" align="central">

<img src="https://github.com/eCloudEdge-Digital/neoedge-central-user-manual/raw/dev/readme-images/account.png" alt="Set Up Account" width="50%" height="auto" align="central">

4. **Verify Successful License Installation:**
   You can confirm that license has been installed successfully by seeing the follwoing message:
   
<img src="https://github.com/eCloudEdge-Digital/neoedge-central-user-manual/raw/dev/readme-images/setup-final.png" alt="Set Up Successfully" width="50%" height="auto" align="central">

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
    

### Further Exploration

For more in-depth information and practical demonstrations, please refer to the following resources:
- [NeoEdge Central Quick Start (English)](https://www.youtube.com/playlist?list=PLUAJDbJOOHqx2JrZCZpMZT_nlDE_qKT2h).
- [NeoEdge Central Quick Start (Chinese)](https://www.youtube.com/playlist?list=PLUAJDbJOOHqzpqJ9g9IN0j4ClaQMbtXE8)
