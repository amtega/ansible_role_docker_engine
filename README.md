# Ansible docker_engine role

This is an [Ansible](http://www.ansible.com) role to setup docker engine.

## Requirements

- Ansible >= 2.0

## Role Variables

A list of all the default variables for this role is available in `defaults/main.yml`.

## Dependencies

None.

## Example Playbook

This is an example playbook:

```yaml
---

- hosts: all
  roles:
    - docker_engine
```

## Testing

```shell
$ cd docker_engine/test
$ ansible-playbook main.yml
```

## License

Not defined.

## Author Information

- Juan Antonio Valiño García ([juanval@edu.xunta.es](mailto:juanval@edu.xunta.es)). Amtega - Xunta de Galicia
