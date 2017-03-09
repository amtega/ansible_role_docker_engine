docker_engine
=============

docker_engine is an [Ansible](http://www.ansible.com) role to setup docker engine

Requirements
------------

- Ansible >= 2.0

Role Variables
--------------

Here is a list of all the default variables for this role, which are also
available in `defaults/main.yml`.

```yaml
---

  # This variables are undefined by default. In this case role will use OS
  # specific variables defined in the <distribution>.yml files within this
  # directory if exist or, alternatively, the default.yml vars.

  # List of packages to install docker
  #
  # docker_engine_packages:

  # List of user to add to docker group. This is usefull to allow concrete users
  # to manage focker without being root

  # docker_engine_users:
```

Dependencies
------------

None.

Example Playbook
----------------

This is an example playbook:

```yaml
---

- hosts: all
  roles:
    - docker_engine  
```

Testing
-------

```shell
$ cd docker_engine
$ ansible-playbook main.yml
```

License
-------

Not defined.

Author Information
------------------

- Juan Antonio Valiño García (<juanval@edu.xunta.es>). Amtega - Xunta de Galicia
