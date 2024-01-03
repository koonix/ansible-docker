# ansible-docker

Ansible roles for installing Docker.

## Roles

### docker

Install the latest versions of Docker and the essential plugins Buildx and Compose,
per [the official instructions](https://docs.docker.com/engine/install).

Supported operating systems:

- Debian
- Ubuntu

#### Variables

| Variable                                        | Description |
|-------------------------------------------------|-------------|
| `docker_daemon_config`                          | Docker daemon's config object to convert to json and place in `/etc/docker/daemon.json`. Default: `{}` |
| `docker_daemon_config_log_rotation`             | Whether to configure the docker daemon to [rotate logs](https://docs.docker.com/config/containers/logging/configure/#configure-the-default-logging-driver). Default: `true` |
