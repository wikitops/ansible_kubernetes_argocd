# Ansible : Playbook ArgoCD

The aim of this project is to deploy ArgoCD on a Kubernetes cluster.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

What things you need to run this Ansible playbook :

*   A running Kubernetes cluster (locally or on cloud)
*   Configure the hosts file based on your architecture. Rename the inventory/hosts.ini in inventory/hosts
*   Download the Ansible requirements:

```bash
$ ansible-galaxy install -r requirements.yml
```

### Usage

A good point with Vagrant is that you can create, update and destroy all architecture easily with some commands.

Be aware that you need to be in the Vagrant directory to be able to run the commands.

#### Deployment

To deploy ArgoCd on Vagrant instances, just run this command :

```bash
$ vagrant up
```

If everything run as expected, you should be able to list the virtual machine created :

```bash
$ vagrant status

Current machine states:

neuvector01                   running (virtualbox)
```

If everything run has expected, you should access :
*   The NeuVector Docs interface : http://10.0.4.81/
*   The NeuVector Console interface : https://10.0.4.81:8443/

#### Destroy

To destroy the Vagrant resources created, just run this command :

```bash
$ vagrant destroy
```

## Author

Member of Wikitops : https://www.wikitops.io/

## Licence

This project is licensed under the Apache License, Version 2.0. For the full text of the license, see the LICENSE file.
