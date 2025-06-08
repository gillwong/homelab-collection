gillwong.homelab.nvidia role
=========

Applies configuration for Linux systems with NVIDIA GPU.

Skip the `reboot` tag if you want to skip system reboot.

Role Variables
--------------

The following variables are required unless stated otherwise.

| Variable | Description | Default |
| -- | -- | -- |
| `nvidia_distro` | System's Linux distribution. Learn more [here](https://docs.nvidia.com/datacenter/tesla/driver-installation-guide/#precompiled-streams). | `rhel9` |
| `nvidia_arch` | System's CPU architecture. Learn more [here](https://docs.nvidia.com/datacenter/tesla/driver-installation-guide/#precompiled-streams). | `x86_64` |
| `nvidia_arch_ext` | System's CPU architecture. Learn more [here](https://docs.nvidia.com/datacenter/tesla/driver-installation-guide/#precompiled-streams). | `x86_64` |
| `nvidia_module_type` | Type of kernel modules to enable. Changing this after running this role may break the system. Values: `open` or `proprietary`. | `proprietary` |

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: nvidia
      roles:
         - role: gillwong.homelab.nvidia
