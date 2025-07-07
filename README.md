# Ansible Role: Deploy Docker Compose

An Ansible Role that deploys a [docker-compose](https://www.docker.com) service.

## Requirements

This role requires docker to be installed on the remote host. I recommend using the `geerlingguy.docker` role to install it. 

## Dependencies

None.

## Role Variables

This role requires two variable,`local_service_dir` the path to the directory where the `docker-compose.yml` resides in and `service_name` to specify the service's name (the prefix for its containers, networks, etc.). 

```yaml
service_name: my_service
local_service_dir: path/to/service/directory/
```

## Example Playbook

```yaml
- hosts: all
  roles:
    - mhorlacher.deploy_docker_compose
```

## License

MIT

## Author Information

This role was created in 2025 by [Marc Horlacher](https://github.com/mhorlacher). 