gillwong.homelab.k8s_base role
=========

Applies base system configuration for Kubernetes nodes.

Skip the `reboot` tag if you want to skip system reboot.

Role Variables
--------------

The following variables are required unless stated otherwise.

| Variable | Description | Default |
| -- | -- | -- |
| `k8s_base_proxy_mode` | kube-proxy [mode](https://kubernetes.io/docs/reference/config-api/kube-proxy-config.v1alpha1/#kubeproxy-config-k8s-io-v1alpha1-ProxyMode). | `iptables` |

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: k8s_cluster
      roles:
         - role: gillwong.homelab.k8s_base
