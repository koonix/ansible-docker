# koonix.docker

Collection of Ansible roles to install Docker.

## Roles

### docker

| Variable                                        | Description |
|-------------------------------------------------|-------------|
| `docker_daemon_config`                          | Docker daemon's config object to convert to json and place in `/etc/docker/daemon.json`. Default: `{}` |
| `docker_daemon_config_log_rotation`             | Whether to configure container logs to be rotated. Default: `true` |
