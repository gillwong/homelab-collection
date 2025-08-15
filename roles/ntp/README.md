gillwong.homelab.ntp role
=========

Applies configuration for Network Time Protocol (NTP).

Role Variables
--------------

The following variables are required unless stated otherwise.

| Variable | Description | Default |
| -- | -- | -- |
| `ntp_chrony_conf` | `chrony.conf` file location. | `/etc/chrony.conf` |
| `ntp_servers` | NTP servers for chronyd inside the node. | See `defaults/main.yml`. |

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: rhel
      roles:
         - role: gillwong.homelab.ntp
