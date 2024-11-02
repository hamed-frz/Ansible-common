# Ansible Backup Automation



This repository contains Ansible configurations and playbooks designed to automate backup tasks for application configurations, MySQL databases, and additional server data. This project leverages Ansible roles and group variables to ensure consistent and reliable backup processes across various components.



## Project Structure



- **`ansible.cfg`**: Configuration file for Ansible, setting inventory and roles paths.

- **`inventory`**: Contains the inventory details of target machines.

- **`group_vars/`**: Variables specific to groups of hosts, defining backup parameters.

- **`playbooks/`**: Contains playbooks for each type of backup:

  - `backup_app.yaml` - Backs up application configuration files.

  - `backup_mysql.yaml` - Backs up MySQL databases.

  - `backup_pf.yaml` - Backs up additional server configurations.

- **`roles/`**: Contains specific roles (`app_backup`, `mysql_backup`, etc.) that define the tasks for each backup type.



## Usage



### Prerequisites



- Ansible must be installed on the control machine.

- SSH access must be configured for all target machines listed in the inventory.

- Ensure proper permissions for backup directories on target machines.



### Running Backups



To execute a backup playbook, use the following command, replacing `<playbook>` with the desired playbook file:



```bash

ansible-playbook playbooks/<playbook>.yaml
