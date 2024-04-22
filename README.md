# Docker Setup Swarm Vagrant

# Technical Report: SwarmVagrantDockerSetup

## Project Description:
The SwarmVagrantDockerSetup project aims to create a local Swarm Cluster environment using Vagrant to provision virtual machines and Docker for container virtualization. The goal is to automate the setup process of a Swarm environment to facilitate the development and testing of distributed applications.

## Technologies Involved:
- **Vagrant**: Used to define and create virtual machines automatically, providing a consistent and replicable configuration.
- **VirtualBox**: Provides virtual machines for Vagrant, used to run the VMs locally.
- **Docker**: Used to create and manage the containers that compose the Swarm cluster. Docker Swarm is a native Docker Engine tool that allows orchestrating multiple containers in a cluster.

## Code Content:
The Vagrantfile.rb file defines the configuration of the virtual machines and their provisioning with Docker. Four virtual machines are created: one "master" machine and three "node" machines, each with Docker pre-installed. The "master" machine is configured as the manager node of the Swarm cluster, while the other machines are configured as worker nodes.

## Usage:
To use the project, simply have Vagrant and VirtualBox installed on the system. Then, create a directory for the project, place the Vagrantfile.rb file inside it, and execute the `vagrant up` command in the terminal. This will create the virtual machines and provision them with Docker. Once provisioning is complete, you will have a ready-to-use local Swarm Cluster environment.

## Implementation:
When the `vagrant up` command is executed, Vagrant starts the process of creating the virtual machines according to the definitions in the Vagrantfile.rb file. VirtualBox is used as the provider of virtual machines. After the VMs are created, Vagrant provisions each of them with Docker, ensuring that all machines have Docker installed and configured correctly. The "master" machine is configured as the manager node of the Swarm cluster, and the other machines are added as worker nodes. Once provisioning is complete, the Swarm Cluster environment is ready to be used.
