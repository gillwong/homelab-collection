gillwong.homelab.gitlab_runner role
=========

Applies configuration for self-managed [GitLab Runners](https://docs.gitlab.com/runner/) with the docker executor.

Role Variables
--------------

The following variables are required unless stated otherwise.

| Variable | Description | Default |
| -- | -- | -- |
| `gitlab_runner_id` | ID of the GitLab Runner. | - |
| `gitlab_runner_token` | Token of the GitLab Runner. | - |
| `gitlab_runner_name` | Name of the GitLab Runner. | `{{ inventory_hostname }}` |
| `gitlab_runner_concurrent` | Concurrent builds allowed. | `4` |

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: gitlab-runner
      roles:
         - role: gillwong.homelab.gitlab_runner
