# ansible-docker

Ansible roles for installing Docker.

## Roles

### docker

Install the latest versions of Docker and the essential plugins Buildx and Compose,
per [the official instructions](https://docs.docker.com/engine/install).

Supported operating systems:

- Debian
- Ubuntu
- Fedora

#### Variables

| Variable                                        | Description |
|-------------------------------------------------|-------------|
| `docker_daemon_config`                          | Docker daemon's config object to convert to json and write to `/etc/docker/daemon.json`. Default: `{}` |
| `docker_daemon_config_log_rotation`             | Whether to configure the docker daemon to [rotate logs](https://docs.docker.com/config/containers/logging/configure/#configure-the-default-logging-driver). Default: `true` |

#### Usage

Example [requirements.yml](https://docs.ansible.com/ansible/latest/galaxy/user_guide.html#installing-roles-and-collections-from-the-same-requirements-yml-file]) file:

```yaml
collections:
  - name: https://github.com/koonix/ansible-docker
    type: git
    version: 0.1.4
```

Example usage in a playbook:

```yaml
- name: Roles
  hosts: all
  roles:
    - koonix.docker.docker
    - ...
```
