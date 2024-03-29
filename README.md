# Ansible docker_engine role

This is an [Ansible](http://www.ansible.com) role to setup docker engine based on oficial docker-ce repositories.

## Role Variables

A list of all the default variables for this role is available in `defaults/main.yml`.

Keep in mind that by default the role could reboot de host to activate kernel parameters introduced in GRUB. To avoid the reboot set `reboot_disable` variable (See `amtega.reboot` role for details).

## Example Playbook

If you want a quick setup on your local machine you can use the `files/setup.yml` playbook:

```shell
$ cd amtega.docker_engine/files
$ ansible-playbook setup.yml --become --ask-become-pass
```

This is an example playbook:

```yaml
---

- hosts: all
  roles:
    - amtega.docker_engine
```

## Testing

Tests are based on [molecule](https://molecule.readthedocs.io/en/latest/installation.html) with vagrant virtual machines.

Once you have vagrant, you can run the tests with the following commands:

```shell
cd amtega.docker_engine

molecule test --all
```

## License

Copyright (C) 2022 AMTEGA - Xunta de Galicia

This role is free software: you can redistribute it and/or modify it under the terms of:

GNU General Public License version 3, or (at your option) any later version; or the European Union Public License, either Version 1.2 or – as soon they will be approved by the European Commission ­subsequent versions of the EUPL.

This role is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details or European Union Public License for more details.

## Author Information

- Juan Antonio Valiño García
- José Enrique Mourón Regueira
