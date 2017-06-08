# Ansible docker_engine role

This is an [Ansible](http://www.ansible.com) role to setup docker engine.

The role is designed to be extended easly loading operating system dependant variables and tasks:

- The role dinamically loads variables applicable to all operating systems from `vars/main.yml` and the specific operating system ones from `vars/{{ ansible_distribution | lower }}*.yml`.

- The role dinamically loads taks applicable to all operating systems from `tasks/install/main.yml`, `tasks/configure/main.yml` and `tasks/service/main.yml`.

- The specific operating system ones are dinamically loaded from the previous tasks dirs looking at the files `{{ ansible_distribution | lower }}*.yml`.

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
