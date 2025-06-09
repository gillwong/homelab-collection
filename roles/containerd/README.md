gillwong.homelab.containerd role
=========

Installs and configures [containerd](https://containerd.io) and [CNI plugins](https://github.com/containernetworking/cni).

Role Variables
--------------

The following variables are required unless stated otherwise.

| Variable | Description | Default |
| -- | -- | -- |
| `containerd_system_arch` | System's CPU architecture. | `amd64` |
| `containerd_runc_version` | [runc](https://github.com/opencontainers/runc) version. | `amd64` |
| `containerd_runc_url` | runc download URL. | `https://github.com/opencontainers/runc/releases/download/v{{ containerd_runc_version }}/runc.{{ containerd_system_arch }}` |
| `containerd_version` | containerd version. | `2.1.1` |
| `containerd_archive` | containerd archive file name. | `containerd-{{ containerd_version }}-linux-{{ containerd_system_arch }}.tar.gz` |
| `containerd_url` | containerd download URL. | `https://github.com/containerd/containerd/releases/download/v{{ containerd_version }}/{{ containerd_archive }}` |
| `containerd_service_url` | containerd service file download URL. | `https://raw.githubusercontent.com/containerd/containerd/main/containerd.service` |
| `containerd_cni_plugins_version` | CNI plugins version. | `1.7.1` |
| `containerd_cni_plugins_archive` | CNI plugins archive file name. | `cni-plugins-linux-{{ containerd_system_arch }}-v{{ containerd_cni_plugins_version }}.tgz` |
| `containerd_cni_plugins_url` | CNI plugins download URL. | `https://github.com/containernetworking/plugins/releases/download/v{{ containerd_cni_plugins_version }}/{{ containerd_cni_plugins_archive }}` |

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: k8s
      roles:
         - role: gillwong.homelab.containerd
