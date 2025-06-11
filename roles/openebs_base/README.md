gillwong.homelab.openebs_base role
=========

Applies base configuration for Kubernetes cluster storage solution [OpenEBS](https://openebs.io).

Skip the `reboot` tag if you want to skip system reboot.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: k8s
      roles:
         - role: gillwong.homelab.openebs_base
