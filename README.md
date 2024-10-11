# Ansible Apache and MariaDB Setup

## Description
This project uses Ansible to automate the installation and configuration of Apache2 and MariaDB on Ubuntu and CentOS servers. The playbooks ensure that the services are properly set up with custom configuration files.

## Prerequisites
- Ansible 2.9 or later
- Access to Ubuntu and CentOS servers

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/YanaDevOps/Ansible_Apache_MariaDB.git
   cd Ansible_Apache_MariaDB
   ```

2. Set up your inventory file in the inventory/ directory.

3. Define your variables in the `group_vars/` and `vars/` directories.

## Running the Playbook
To run the playbook, execute the following command:
   ```bash
   ansible-playbook -i inventory/hosts.ini main.yml
   ```

## Project Structure
```bash
Ansible_Apache_MariaDB/
├── inventory/
│   └── hosts.ini           # Inventory file with server details
├── group_vars/             # Directory for group variable files
│   ├── ubuntu_servers.yml
│   └── centos_servers.yml
├── roles/                  # Roles for Apache and MariaDB
│   ├── apache2/
│   │   ├── tasks/
│   │   ├── handlers/
│   │   └── templates/
│   └── mariadb/
│       ├── tasks/
│       ├── handlers/
│       └── templates/
└── main.yml                # Main playbook
```

## Features
* Automates the installation and configuration of Apache2.
* Sets up MariaDB with a custom configuration.
* Uses Jinja2 templates for configuration files.

## Technologies Used
* Ansible
* Apache
* MariaDB

## Author
Name: Yana Lysenko
