gillwong.homelab.base role
=========

Applies base configuration for machines in the homelab.

Role Variables
--------------

The following variables are required unless stated otherwise.

| Variable | Description | Default |
| -- | -- | -- |
| `base_chrony_conf` | chrony configuration file path | `/etc/chrony.conf` |
| `base_ntp_servers` | NTP servers for chronyd inside the machine. | See `defaults/main.yaml`. |

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: homelab
      roles:
         - role: gillwong.homelab.base
