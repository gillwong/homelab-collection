gillwong.homelab.kubeadm_init role
=========

Bootstraps the first Kubernetes control plane node using `kubeadm init` and installs the pod networking solution [Calico](https://www.tigera.io/project-calico/).

Role Variables
--------------

The following variables are required unless stated otherwise.

| Variable | Description | Default |
| -- | -- | -- |
| `kubeadm_init_service_subnet` | Kubernetes Services subnet CIDR. | `10.96.0.0/12` |
| `kubeadm_init_pod_subnet` | Kubernetes Pods subnet CIDR. | `10.244.0.0/16` |
| `kubeadm_init_cluster_endpoint` | Kubernetes cluster endpoint. | - |
| `kubeadm_init_extra_sans` | A list of additional SANs for the cluster endpoint. | `[]` |
| `kubeadm_init_proxy_mode` | kube-proxy [mode](https://kubernetes.io/docs/reference/config-api/kube-proxy-config.v1alpha1/#kubeproxy-config-k8s-io-v1alpha1-ProxyMode). | `iptables` |

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: k8s-cp-1
      roles:
         - role: gillwong.homelab.kubeadm_init
