# Nginx Installation and Setup

This repository contains an Ansible playbook that automates the installation and setup of Nginx on target servers. The playbook updates DNS nameservers, installs Nginx, and starts the Nginx service.

## Prerequisites

Before using this playbook, ensure that you meet the following prerequisites:

- Ansible is installed on the control machine. If not, you can install it by following the official [Ansible Installation Guide](https://docs.ansible.com/ansible/latest/installation_guide/index.html).

- You have SSH access to the target server(s) where you want to install Nginx. Make sure the necessary SSH keys and credentials are configured.

## Usage

1. Edit the `inventory.ini` file and specify the IP address or hostname of the target server(s) under the `nginx` group. If deploying to multiple servers, ensure they are all listed.

2. Run the Ansible playbook to install and set up Nginx:

   ```bash
   ansible-playbook -i inventory.ini playbook.yml
   ```

   Ansible will connect to the target server(s), update the DNS nameservers, update the apt repository and cache, install Nginx, and start the Nginx service.

## Customization

Feel free to customize the playbook according to your specific needs. You can modify the DNS nameservers, add additional tasks or configurations, and adapt the Nginx installation and setup as required.

## Contributing

Contributions are welcome! If you have any improvements or suggestions, please feel free to submit a pull request. Ensure that your changes align with the existing coding style and include relevant documentation.

## License

This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and distribute this playbook as per the terms of the license.

---
