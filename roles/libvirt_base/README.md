gillwong.homelab.libvirt_base role
=========

Applies base configuration for libvirt hosts.

Role Variables
--------------

The following variables are required unless stated otherwise.

| Variable | Description | Default |
| -- | -- | -- |
| `libvirt_base_pool_name` | Storage pool name. | `lvmpool` |
| `libvirt_base_vg_name` | Volume group name to create the storage pool from. | `rhel` |

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: rhel
      roles:
         - role: gillwong.homelab.libvirt_base
