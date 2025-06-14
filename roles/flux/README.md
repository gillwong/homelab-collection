gillwong.homelab.flux role
=========

Installs [Flux CD](https://fluxcd.io).

Role Variables
--------------

The following variables are required unless stated otherwise.

| Variable | Description | Default |
| -- | -- | -- |
| `flux_version` | Flux version. | `2.6.1` |
| `flux_git_provider` | Flux bootstrap git provider. | `github` |
| `flux_git_token` | GitHub or GitLab PAT with permissions for Flux to create the GitOps repository. | - |
| `flux_git_username` | Git username. | - |
| `flux_git_repository` | Git repository. | - |
| `flux_git_branch` | Git branch. | `main` |
| `flux_git_path` | Path inside the repository to create the Flux manifests. | `clusters/homelab` |

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: k8s-cp-1
      roles:
         - role: gillwong.homelab.flux
