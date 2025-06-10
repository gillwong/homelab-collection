gillwong.homelab.os role
=========

Asserts that the system is of the given OS.

Role Variables
--------------

The following variables are required unless stated otherwise.

| Variable | Description | Default |
| -- | -- | -- |
| `os_distro` | Operating system. | `RedHat` |

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - role: gillwong.homelab.os
           vars:
             os_distro: RedHat
