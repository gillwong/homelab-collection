gillwong.homelab.update_libosinfo role
=========

Updates the local [libosinfo](https://libosinfo.org) database directly from the [download site](https://releases.pagure.org/libosinfo/?C=M;O=D).

Role Variables
--------------

The following variables are required unless stated otherwise.

| Variable | Description | Default |
| -- | -- | -- |
| `update_libosinfo_version` | libosinfo database version. | - |
| `update_libosinfo_url` | libosinfo database URL. | `https://releases.pagure.org/libosinfo/osinfo-db-{{ update_libosinfo_version }}.tar.xz` |

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: rhel
      roles:
         - role: gillwong.homelab.update_libosinfo
