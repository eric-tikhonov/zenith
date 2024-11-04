# Zenith Homelab

## Description
Zenith is a comprehensive homelab setup leveraging Kubernetes, Ansible, and Terraform to deploy and manage self-hosted services and applications securely and efficiently.

## Table of Contents
- [Project Structure](#project-structure)
- [Technologies and Tools](#technologies-and-tools)
- [Applications](#applications)
- [Installation and Setup](#installation-and-setup)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Project Structure
```plaintext
zenith/
├── .gitignore
├── README.md
├── ansible/
│   ├── playbooks/
│   │   ├── site.yml
│   │   ├── roles/
│   │   │   ├── common/
│   │   │   │   ├── tasks/
│   │   │   │   ├── handlers/
│   │   │   │   ├── templates/
│   │   │   │   ├── files/
│   │   │   │   ├── vars/
│   │   │   ├── kubernetes/
│   │   │   ├── nextcloud/
│   │   │   ├── pfsense/
│   │   │   ├── suricata/
│   │   │   ├── homarr/
├── terraform/
│   ├── main.tf
│   ├── variables.tf
│   ├── outputs.tf
│   ├── modules/
│   │   ├── kubernetes/
│   │   ├── network/
│   │   ├── storage/
├── config/
│   ├── nextcloud/
│   │   ├── config.php
│   ├── pfsense/
│   │   ├── config.xml
│   ├── suricata/
│   │   ├── suricata.yaml
│   ├── homarr/
│   │   ├── config.json
│   ├── kubernetes/
│   │   ├── deployment.yaml
│   │   ├── service.yaml
├── scripts/
│   ├── setup.sh
│   ├── deploy.sh
```
## Technologies and Tools
Ubuntu Server

Kubernetes

Ansible

Terraform

Docker

Nginx

Certbot

## Applications
Homarr: Modern dashboard for managing services

Bitwarden: Password manager

AdGuard Home: Ads & trackers blocking DNS server

Pi-hole: VPN and local DNS server

Nextcloud: File storage and calendar sync

PfSense: Firewall

Suricata: Network security monitoring

## Installation and Setup
### Prerequisites
Domain Name: Register a domain and configure DNS.

Public IP: Ensure your server has a public IP address.

### Step-by-Step Guide
Clone the Repository
```
git clone https://github.com/yourusername/zenith.git
cd zenith
```

Run Setup Script
```
./scripts/setup.sh
```

Deploy Infrastructure with Terraform
```
cd terraform
terraform init
terraform apply
```

Configure Servers with Ansible
```
cd ../ansible
ansible-playbook playbooks/site.yml
```

Set Up Nginx and Obtain SSL Certificates
```
sudo certbot --nginx -d zenith.erictikhonov.com
```

### Usage
Access the Homarr Dashboard

Navigate to https://zenith.erictikhonov.com to manage your services.

Monitor and Manage Services

Use the web interfaces for each application (e.g., Nextcloud, Bitwarden).

### Contributing
Contributions are welcome! Please fork the repository and submit a pull request.

### License
This project is licensed under the MIT License.

### Contact
For any questions or feedback, please contact Eric Tikhonov.
