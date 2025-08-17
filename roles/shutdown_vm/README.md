gillwong.homelab.shutdown_vm role
=========

Shuts down a VM.

Role Variables
--------------

The following variables are required unless stated otherwise.

| Variable | Description | Default |
| -- | -- | -- |
| `shutdown_vm_name` | Virtual machine name. | - |

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: rhel
      roles:
         - role: gillwong.homelab.shutdown_vm
           vars:
             shutdown_vm_name: testvm
