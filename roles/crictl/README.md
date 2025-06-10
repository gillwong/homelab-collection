gillwong.homelab.crictl role
=========

Installs and configures [crictl](https://github.com/kubernetes-sigs/cri-tools).

Role Variables
--------------

The following variables are required unless stated otherwise.

| Variable | Description | Default |
| -- | -- | -- |
| `crictl_download_dir` | Download directory on the Ansible controller node. | - |
| `crictl_system_arch` | System architecture. | `amd64` |
| `crictl_version` | crictl version. | `1.33.0` |
| `crictl_archive` | crictl archive file name. | `crictl-v{{ crictl_version }}-linux-{{ crictl_system_arch }}.tar.gz` |

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: k8s
      roles:
         - role: gillwong.homelab.crictl
