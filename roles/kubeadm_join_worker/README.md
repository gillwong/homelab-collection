gillwong.homelab.kubeadm_join_worker role
=========

Joins the machine to an existing Kubernetes cluster as a Kubernetes worker node.

Role Variables
--------------

The following variables are required unless stated otherwise.

| Variable | Description | Default |
| -- | -- | -- |
| `kubeadm_join_worker_cluster_endpoint` | Kubernetes cluster endpoint. | - |
| `kubeadm_join_worker_token` | kubeadm join token. | - |
| `kubeadm_join_worker_ca_cert_hash` | kubeadm join CA certificate hash. | - |

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: k8s_worker
      roles:
         - role: gillwong.homelab.kubeadm_join_worker
