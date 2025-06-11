gillwong.homelab.kubeadm_join_cp role
=========

Joins the machine to an existing Kubernetes cluster as a Kubernetes control plane node.

Role Variables
--------------

The following variables are required unless stated otherwise.

| Variable | Description | Default |
| -- | -- | -- |
| `kubeadm_join_cp_cluster_endpoint` | Kubernetes cluster endpoint. | - |
| `kubeadm_join_cp_token` | kubeadm join token. | - |
| `kubeadm_join_cp_ca_cert_hash` | kubeadm join CA certificate hash. | - |
| `kubeadm_join_cp_ca_key` | kubeadm join CA key for control plane. | - |

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts:
        - k8s-cp-2
        - k8s-cp-3
      roles:
         - role: gillwong.homelab.kubeadm_join_cp
