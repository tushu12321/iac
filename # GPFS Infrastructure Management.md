# GPFS Infrastructure Management

This repository contains infrastructure code to manage IBM Spectrum Scale (GPFS) clusters. The code is designed to automate the deployment, configuration, and management of GPFS clusters.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites

Before you begin, ensure you have met the following requirements:

- You have a Linux-based operating system.
- You have `ansible` installed on your local machine.
- You have access to the GPFS installation packages.

## Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/yourusername/gpfs-infrastructure.git
    cd gpfs-infrastructure
    ```

2. Install the required Ansible roles:

    ```sh
    ansible-galaxy install -r requirements.yml
    ```

## Usage

To deploy a GPFS cluster, follow these steps:

1. Update the inventory file with your cluster nodes:

    ```ini
    [gpfs_nodes]
    node1 ansible_host=192.168.1.1
    node2 ansible_host=192.168.1.2
    node3 ansible_host=192.168.1.3
    ```

2. Run the Ansible playbook to install and configure GPFS:

    ```sh
    ansible-playbook -i inventory gpfs.yml
    ```

## Configuration

The configuration files are located in the `config` directory. You can customize the GPFS settings by editing the following files:

- `gpfs.conf`: Main configuration file for GPFS.
- `mmsdrfs`: File system configuration file.
- `nsddevices`: NSD (Network Shared Disk) configuration file.

## Contributing

Contributions are welcome! Please read the CONTRIBUTING.md file for guidelines on how to contribute to this project.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.