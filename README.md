# NeoEdge Central Enterprise Edition
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
NeoEdge Central Enterprise Edition is supported on **Linux (amd64 architecture)**.
    - For optimal stability and reliability, we highly recommend using **Ubuntu 22.04 LTS**.
    
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

  With the above resources, it would be easy to support 10,000 IoT gateways connected and sending messages simultaneously at a rate of one message per second.
  
* **TPM2.0 Requirements:**
TPM2.0 is mandatory for NeoEdge Central Enterprise Edition to encrypt and protect essential data and keys. Please ensure your machine or virtual machine is equipped with TPM2.0.
    - For Azure, please refer to <a href="https://learn.microsoft.com/en-us/azure/virtual-machines/trusted-launch">this doc</a> to enable trusted launch on VM.
    - For AWS, please refer to <a href="https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/nitrotpm.html">this doc</a> to enable NitroTPM on EC2.
    - For GCP, please refer to <a href="https://cloud.google.com/compute/shielded-vm/docs/shielded-vm#vtpm">this doc</a> to enable vTPM on GCP VM.

* **Docker& Docker Compose:** 
Before installing NeoEdge Central Enterprise Edition, ensure you have **Docker Engine and Docker Compose** installed. 
    - Detailed installation instructions for your specific operating system can be found on the [official Docker website](https://docs.docker.com/engine/install/).
    - For optimal stability and reliability, we highly recommend using **Docker Engine Version 28.1** and **Docker Compose Version v2.35**.
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
1.  **Download NeoEdge Central Installer:**
    Select and download the NeoEdge Central Installer that matches your needs.

    - To download the latest version of NeoEdge Central installer:
    
    ```bash
    sudo wget https://download.ecloudedge.com/neoedge/latest/installer.tar.gz
    ```
    - To download a specific version of NeoEdge Central installer:

    ```bash
    sudo wget https://download.ecloudedge.com/neoedge/neoedge-central-version/installer.tar.gz
    ```
    Replace `neoedge-central-version` with the specific version for installation. For example, `https://download.ecloudedge.com/neoedge/1.0.0/installer.tar.gz`.
    
    For a list of available versions, refer to the [NeoEdge Central Enterprise Edition release notes](https://www.ecloudedge.com/neoedge-central-enterprise-edition-release-notes/).
    
2.  **Extract the Installer:**
    Unpack the installer.tar.gz archive into a dedicated installer directory using the following command:
    
    ```bash
    sudo tar xfvz installer.tar.gz
    ```
3. **Execute the Installer:**
   Navigate into the newly created installer directory and run the installer-linux-amd64 executable. The estimated installation time is approximately 10 minutes:
   ```bash
   cd installer
   sudo ./installer-linux-amd64 -domain <domain> 
   ```
   ```text
   Available command line options 
   -h
    Help
   -domain <domain>
    Required. Domain name of your NeoEdge Central server, specified as either the IP address of the installed machine or a resolvable DNS domain name associated with it.
   -loglevel <log level>
    Optional (default "error").Log level including error, warn, info, debug. 
   -mode <mode>
    Optional (default "cli"). Mode to run the installer,including tui (text-based user interface) or cli (command-line interface). 
   ```
4. **Verify Successful Installation:**
   You can confirm that NeoEdge Central Enterprise Edition has been installed successfully by checking for a specific message in either the installer.log file or the standard output displayed during the installation process. 

   Look for the following confirmation:
   ```bash
   #standard output 
   Installation completed successfully.

   #installer.log message
   {"time":"*","level":"INFO","msg":"Installation completed successfully."}
   ```

4. **Configure Your Firewall:**
   The following firewall policies are mandatory on your NeoEdge Central server:
    
    | Source IP  | Source Port | Destination IP | Destination Port  
    | --------   | -------- | -------- | -------- | 
    | Any or your Browser | Any | ```<neoedge-central-ip>``` | 443/TCP 
    | Any or Gateway | Any | ```<neoedge-central-ip>``` | 8443/TCP 
    | Any or Gateway | Any | ```<neoedge-central-ip>``` | 8883/TCP
    

### License Application 
NeoEdge Central Enterprise Edition requires a valid license for use. Please follow these steps to apply: 

1. **Download License Request File:**
   To apply for a license, you must first download a license request file. Open your web browser and navigate to the NeoEdge Central license page: 
  
   ```bash
   https://neoedge-central-domain/license
   ```
    Replace `neoedge-central-domain` with the domain name of your neoedge central server.

      <img src="https://github.com/eCloudEdge-Digital/neoedge-central-user-manual/raw/dev/readme-images/license-request.png" alt="License Request" width="95%" 
      height="auto" align="center" margin="20px">


---

📣 **Reminder:**   
* **Use the latest downloaded license request file:**  If you've generated the license request file multiple times, please use the most recent version for your application, as each generation creates unique license content.

---

2. **Start Your License Application:**
   To ensure you receive the correct license, please first decide the number of gateways and advanced apps your deployment requires.

   Once you have this information, please have your downloaded license request file ready and contact your ECE sales representative to start your application.

   If you have any questions or need further clarification, please don't hesitate to contact us at [sales@ecloudedge.com](mailto:sales@ecloudedge.com).

3. **Install NeoEdge Central License:**
   After license is issued, please upload the received license key file to install the license and set up the initial user account and password.

    <img src="https://github.com/eCloudEdge-Digital/neoedge-central-user-manual/raw/dev/readme-images/license-file-upload.png" alt="License Upload" width="95%" height="auto" align="central" margin="20px">
    
    <img src="https://github.com/eCloudEdge-Digital/neoedge-central-user-manual/raw/dev/readme-images/add-account.png" alt="Set Up Account" width="95%" height="auto" align="central" margin="40px">

4. **Verify Successful License Installation:**
   You can confirm that license has been installed successfully by seeing the follwoing message:
   
    <img src="https://github.com/eCloudEdge-Digital/neoedge-central-user-manual/raw/dev/readme-images/setup-final.png" alt="Set Up Successfully" width="95%" height="auto" align="central" margin="20px">

### Uninstallation Steps  

1. **Uninstall:**
   Uninstall NeoEdge Central by executing the following command. You'll then be prompted to decide if you want to keep your configuration files, such as your license and data:

    ```bash
    # uninstall NeoEdge Central by executing the following command
    cd /opt/neoedgecentral && sudo ./uninstaller-linux-amd64 
    ```
   
    ```bash
    # choose whether to keep you configuration files
    Do you want to keep the configuration files? (yes/no): 
    ```
2. **Verify Successful Uninstallation:**
    You can confirm that NeoEdge Central has been uninstalled successfully by checking for a specific message in the standard output displayed during the uninstallation process. 

    Look for the following confirmation:

   ```bash
   #standard output 
   Uninstallation process completed.
   ``` 

## Getting Started
Once the installation is complete, you can access and begin using NeoEdge Central.


### Basic Usage
1. **Accessing NeoEdge Central:**
Open your web browser and navigate to the NeoEdge Central login page: 

```bash
https://neoedge-central-domain/login
```
Replace `neoedge-central-domain` with the domain name of your neoedge central server.

![Website Screenshot](https://github.com/eCloudEdge-Digital/neoedge-central-user-manual/raw/dev/readme-images/user-login.png)
    


### Further Exploration

For more in-depth information and practical demonstrations, please refer to the following resources:
- [NeoEdge Central Quick Start (English)](https://www.youtube.com/playlist?list=PLUAJDbJOOHqx2JrZCZpMZT_nlDE_qKT2h).
- [NeoEdge Central Quick Start (Chinese)](https://www.youtube.com/playlist?list=PLUAJDbJOOHqzpqJ9g9IN0j4ClaQMbtXE8)
