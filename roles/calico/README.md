gillwong.homelab.calico role
=========

Installs pod networking solution [Calico](https://www.tigera.io/project-calico/) in a Kubernetes cluster.

Role Variables
--------------

The following variables are required unless stated otherwise.

| Variable | Description | Default |
| -- | -- | -- |
| `calico_version` | Calico version. | `3.30.1` |
| `calico_tigera_operator_url` | Base URL for Tigera operator manifests. | `https://raw.githubusercontent.com/projectcalico/calico/v{{ calico_version }}/manifests` |
| `calico_pod_subnet` | Kubernetes Pods subnet CIDR | `10.244.0.0/16` |
| `calico_kube_proxy_mode` | kube-proxy [mode](https://kubernetes.io/docs/reference/config-api/kube-proxy-config.v1alpha1/#kubeproxy-config-k8s-io-v1alpha1-ProxyMode). | `iptables` |

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: k8s-cp-1
      roles:
         - role: gillwong.homelab.calico
