gillwong.homelab.kubeadm_post role
=========

Configure `kubectl` kubeconfig after running `kubeadm init/join`.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: k8s-cp-1
      roles:
         - role: gillwong.homelab.kubeadm_post
