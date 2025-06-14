# Homelab Ansible Collection

[![CI](https://github.com/gillwong/homelab-collection/actions/workflows/ci.yaml/badge.svg)](https://github.com/gillwong/homelab-collection/actions/workflows/ci.yaml) [![Release](https://github.com/gillwong/homelab-collection/actions/workflows/release.yaml/badge.svg?event=release)](https://github.com/gillwong/homelab-collection/actions/workflows/release.yaml)

A comprehensive collection of Ansible roles for managing and automating my homelab infrastructure.

## Scope

This Ansible collection contains roles dedicated to

- Configuring Proxmox Virtual Environment nodes
- Applying base configuration to Proxmox VMs
- Installing video graphics drivers
- Bootstraping a Kubernetes cluster

## Installation

1. Ensure you have [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/index.html) and the `ansible-galaxy` CLI installed on your control node.
2. Install this Ansible collection:

```bash
ansible-galaxy collection install gillwong.homelab
```

## Usage

You can use the roles in this collection by referencing them in your playbooks. Example usage can be found in [this repo](https://github.com/gillwong/homelab-playbooks).

## Customization

Each role provides default variables that you can override in your playbooks or inventory. See the `defaults/main.yml` file in each role directory for available options.

Example:

```yaml
# Override variables in your playbook or inventory
override_var: value
```

## Included Roles

- **base**: Base system configuration
- **calico**: Installs and configures Calico networking for Kubernetes
- **calico_base**: Base system configuration for Calico
- **containerd**: Installs and configures containerd runtime
- **crictl**: Installs and configures crictl tool
- **flux**: Installs and configures Flux for GitOps
- **gitlab_runner**: Installs and configures GitLab Runner
- **k8s_base**: Base configuration for Kubernetes nodes
- **k8s_cp_base**: Control plane base configuration
- **k8s_download**: Handles Kubernetes binary downloads
- **k8s_tools**: Installs Kubernetes CLI tools and dependencies
- **kubeadm_init**: Handles kubeadm cluster initialization
- **kubeadm_join_cp**: Handles joining control plane nodes
- **kubeadm_join_worker**: Handles joining worker nodes
- **kubeadm_post**: Post-initialization tasks for kubeadm
- **nvidia**: Installs NVIDIA drivers and tools
- **nvidia_containerd**: NVIDIA containerd integration
- **openebs_base**: Installs and configures OpenEBS storage
- **os**: OS-specific configuration
- **pve**: Proxmox VE node base configuration

See each role's `README.md` for more details and available variables.
