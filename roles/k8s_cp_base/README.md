gillwong.homelab.k8s_cp_base role
=========

Applies base system configuration for Kubernetes control plane nodes.

Skip the `reboot` tag if you want to skip system reboot.

Role Variables
--------------

The following variables are required unless stated otherwise.

| Variable | Description | Default |
| -- | -- | -- |
| `k8s_cp_base_cluster_endpoint` | Kubernetes cluster endpoint IP address. | - |
| `k8s_cp_base_kube_vip_version` | kube-vip version. | `0.9.1` |

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: k8s_cp
      roles:
         - role: gillwong.homelab.k8s_cp_base
