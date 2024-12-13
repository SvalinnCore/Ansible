# Ansible Repository Documentation

## Overview
This Git repository contains the complete Ansible setup for deploying and managing an Active Directory environment. It includes all necessary playbooks, inventories, roles, and configurations to automate the deployment and maintenance of an AD infrastructure.

## Repository Contents

- **Playbooks**: YAML files that define tasks for configuring and managing the infrastructure.
- **Inventories**: Files and directories for organizing host and group variables.
- **Roles**: Modular components for reusable Ansible code.
- **Configuration Files**: Custom Ansible configurations for optimizing execution and environment setup.

## Directory Structure
The repository is organized as follows:
```
ansible/
|-- inventories/
|   |-- devel/
|       |-- group_vars/
|       |-- host_vars/
|       `-- inventory.yml
|-- playbooks/
|   `-- example_playbook.yml
|-- roles/
|-- ansible.cfg
```

## Usage

### Verifying the Setup
Ensure the control host can communicate with target hosts:
```bash
ansible all -m ping
```
For Windows hosts:
```bash
ansible all -m win_ping
```

### Running Playbooks
Example to configure a domain controller:
```bash
ansible-playbook playbooks/setup_dc.yml
```

## Additional Information
- Detailed documentation is available in the [Ansible Documentation](https://docs.ansible.com/).
