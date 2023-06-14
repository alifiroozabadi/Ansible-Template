# Rocket.Chat Docker Deployment

This repository contains an Ansible playbook that automates the deployment of a Rocket.Chat instance using Docker. The playbook sets up the necessary dependencies, configures the DNS nameservers, adds the Docker repository, installs Docker, installs Docker Compose, and starts Rocket.Chat using a Docker Compose file.

## Prerequisites

Before using this playbook, make sure you have met the following prerequisites:

- Ansible is installed on the control machine. If not, you can install it by following the official [Ansible Installation Guide](https://docs.ansible.com/ansible/latest/installation_guide/index.html).

- You have SSH access to the target server(s) where you want to deploy Rocket.Chat. Ensure that the necessary SSH keys and credentials are configured.

## Usage

1. Edit the `inventory.ini` file and specify the IP address or hostname of the target server(s) under the `rocket` group. If deploying to multiple servers, ensure they are all listed.

2. Run the Ansible playbook to deploy Rocket.Chat:

   ```bash
   ansible-playbook -i inventory.ini playbook.yml
   ```

   Ansible will connect to the target server(s), install the required dependencies, update the DNS nameservers, add the Docker repository, install Docker and Docker Compose, create the Docker Compose file for Rocket.Chat, and start the Rocket.Chat container.

## Customization

Feel free to customize the playbook according to your specific needs. You can modify the DNS nameservers, add additional tasks or configurations, adapt the Rocket.Chat Docker Compose file, and customize environment variables as required.

Note: Some lines in the playbook are commented out (e.g., adding user to Docker group). Uncomment and modify those lines if you need to include them in your deployment.

## Contributing

Contributions are welcome! If you have any improvements or suggestions, please feel free to submit a pull request. Ensure that your changes align with the existing coding style and include relevant documentation.

## License

This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and distribute this playbook as per the terms of the license.

---
