gillwong.homelab.k8s_base role
=========

Applies base system configuration for Kubernetes nodes.

Skip the `reboot` tag if you want to skip system reboot.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: k8s_cluster
      roles:
         - role: gillwong.homelab.k8s_base
