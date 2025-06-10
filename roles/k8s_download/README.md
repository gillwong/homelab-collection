gillwong.homelab.k8s_download role
=========

Downloads the following in parallel:

- runc
- containerd
- CNI plugins
- crictl

Role Variables
--------------

The following variables are required unless stated otherwise.

| Variable | Description | Default |
| -- | -- | -- |
| `k8s_download_dir` | Download directory. | - |
| `k8s_download_system_arch` | System architecture. | `amd64` |
| `k8s_download_runc_version` | [runc](https://github.com/opencontainers/runc) version. | `amd64` |
| `k8s_download_runc_url` | runc download URL. | `https://github.com/opencontainers/runc/releases/download/v{{ k8s_download_runc_version }}/runc.{{ k8s_download_system_arch }}` |
| `k8s_download_containerd_version` | containerd version. | `2.1.1` |
| `k8s_download_containerd_archive` | containerd archive file name. | `containerd-{{ k8s_download_containerd_version }}-linux-{{ k8s_download_system_arch }}.tar.gz` |
| `k8s_download_containerd_url` | containerd download URL. | `https://github.com/containerd/containerd/releases/download/v{{ k8s_download_containerd_version }}/{{ k8s_download_containerd_archive }}` |
| `k8s_download_containerd_service_url` | containerd service file download URL. | `https://raw.githubusercontent.com/containerd/containerd/main/containerd.service` |
| `k8s_download_cni_plugins_version` | CNI plugins version. | `1.7.1` |
| `k8s_download_cni_plugins_archive` | CNI plugins archive file name. | `cni-plugins-linux-{{ k8s_download_system_arch }}-v{{ k8s_download_cni_plugins_version }}.tgz` |
| `k8s_download_cni_plugins_url` | CNI plugins download URL. | `https://github.com/containernetworking/plugins/releases/download/v{{ k8s_download_cni_plugins_version }}/{{ k8s_download_cni_plugins_archive }}` |
| `k8s_download_crictl_version` | crictl version. | `1.33.0` |
| `k8s_download_crictl_archive` | crictl archive file name. | `crictl-v{{ k8s_downloadcrictl_version }}-linux-{{ k8s_downloadcrictl_system_arch }}.tar.gz` |
| `k8s_download_crictl_url` | crictl download URL. | `https://github.com/kubernetes-sigs/cri-tools/releases/download/v{{ k8s_downloadcrictl_version }}/{{ k8s_downloadcrictl_archive }}` |

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: k8s
      roles:
         - role: gillwong.homelab.crictl
