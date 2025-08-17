gillwong.homelab.create_almalinux_vm role
=========

Creates and starts an Almalinux 10 VM.

Role Variables
--------------

The following variables are required unless stated otherwise.

| Variable | Description | Default |
| -- | -- | -- |
| `create_almalinux_vm_name` | Virtual machine name. | - |
| `create_almalinux_vm_fqdn` | Virtual machine FQDN. | Value of `create_almalinux_vm_name`. |
| `create_almalinux_vm_pubkeys` | A list of SSH authorized keys. | - |
| `create_almalinux_vm_pool` | Storage pool to use for the virtual machine's storage volume. | - |
| `create_almalinux_vm_ipv4s` | A list of IPv4 addresses of the virtual machine. | - |
| `create_almalinux_vm_qcow2_path` | Path of the Almalinux 10 QCOW2 cloud image. | See `defaults/main.yml`. |
| `create_almalinux_vm_vg` | The volume group containing the logical volume where the virtual machine's storage volume is. | `rhel` |
| `create_almalinux_vm_mem_mib` | Virtual machine's memory/RAM in MiB. | `2048` |
| `create_almalinux_vm_vcpus` | Virtual machine's virtual CPU cores. | `1` |
| `create_almalinux_vm_vol_cap_g` | Virtual machine's storage volume capacity in G. | `20` |
| `create_almalinux_vm_bridge` | Host's network bridge name for the virtual machine's networking. | `br0` |
| `create_almalinux_vm_gateway_ipv4` | IPv4 address of the gateway. | `192.168.0.1` |
| `create_almalinux_vm_nameservers_ipv4` | A list of IPv4 addresses of the nameservers. | `[192.168.0.1]` |

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: rhel
      roles:
         - role: gillwong.homelab.create_almalinux_vm
