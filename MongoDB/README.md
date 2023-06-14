# MongoDB Docker Deployment

This repository contains an Ansible playbook that automates the deployment of a MongoDB Docker container. The playbook sets up the necessary dependencies, configures the DNS nameservers, adds the Docker repository, and installs Docker and the required Python package.

## Prerequisites

Before using this playbook, make sure you have met the following prerequisites:

- Ansible is installed on the control machine. If not, you can install it by following the official [Ansible Installation Guide](https://docs.ansible.com/ansible/latest/installation_guide/index.html).

- You have SSH access to the target server(s) where you want to deploy the MongoDB Docker container. Ensure that the necessary SSH keys and credentials are configured.

## Usage

1. Edit the `inventory.ini` file and specify the IP address or hostname of the target server(s) under the `mongodb` group. If deploying to multiple servers, ensure they are all listed.

2. Run the Ansible playbook to deploy MongoDB:

   ```bash
   ansible-playbook -i inventory.ini playbook.yml
   ```

   Ansible will connect to the target server(s), install the required dependencies, update the DNS nameservers, add the Docker repository, install Docker, and create a MongoDB container.

## Customization

Feel free to customize the playbook according to your specific needs. You can modify the DNS nameservers, add additional tasks or configurations, and adapt the MongoDB container settings as required.

Note: Some lines in the playbook are commented out (e.g., adding user to Docker group). Uncomment and modify those lines if you need to include them in your deployment.

## Contributing

Contributions are welcome! If you have any improvements or suggestions, please feel free to submit a pull request. Ensure that your changes align with the existing coding style and include relevant documentation.

## License

This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and distribute this playbook as per the terms of the license.

---

This README file provides clear instructions on how to use the Ansible playbook for deploying MongoDB using Docker. It also includes information on customization, contributing, and licensing. Feel free to modify this template to suit your repository's requirements.
