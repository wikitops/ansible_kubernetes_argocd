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

#### Deployment

To deploy ArgoCd on Kubernetes instances, just run this command :

```bash
$ ansible-playbook argocd.yml
```

If everything run has expected, you should access ArgoCD dashboard depending on the Kubernetes port attribution.

#### Destroy

To destroy the ArgoCD resources created, just follow these steps :

```yaml
# First change the default Ansible variable in the roles/argocd/defaults/main.yml file

# Action
argocd_action: absent
```

Save the change and run the Ansible playbook :

```bash
$ ansible-playbook argocd.yml
```

## Author

Member of Wikitops : https://www.wikitops.io/

## Licence

This project is licensed under the Apache License, Version 2.0. For the full text of the license, see the LICENSE file.
