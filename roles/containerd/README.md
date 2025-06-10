gillwong.homelab.containerd role
=========

Installs and configures [containerd](https://containerd.io) and [CNI plugins](https://github.com/containernetworking/cni).

Role Variables
--------------

The following variables are required unless stated otherwise.

| Variable | Description | Default |
| -- | -- | -- |
| `containerd_download_dir` | Download directory on the Ansible controller node. | - |
| `containerd_system_arch` | System's CPU architecture. | `amd64` |
| `containerd_runc_version` | [runc](https://github.com/opencontainers/runc) version. | `amd64` |
| `containerd_version` | containerd version. | `2.1.1` |
| `containerd_archive` | containerd archive file name. | `containerd-{{ containerd_version }}-linux-{{ containerd_system_arch }}.tar.gz` |
| `containerd_cni_plugins_version` | CNI plugins version. | `1.7.1` |
| `containerd_cni_plugins_archive` | CNI plugins archive file name. | `cni-plugins-linux-{{ containerd_system_arch }}-v{{ containerd_cni_plugins_version }}.tgz` |

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: k8s
      roles:
         - role: gillwong.homelab.containerd
