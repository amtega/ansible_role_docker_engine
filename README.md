docker_engine
=============

This is an [Ansible](http://www.ansible.com) role to setup docker engine.

Requirements
------------

- Ansible >= 2.0

Role Variables
--------------

Here is a list of all the default variables for this role, which are also
available in `defaults/main.yml`.

```yaml
---
  # List of users to add to docker group. This is usefull to allow concrete users
  # to manage focker without being root

  docker_engine_users: []

  # Docker storage parameters
  # See /usr/lib/docker-storage-setup/docker-storage-setup for details

  docker_engine_storage_driver: ""
  docker_engine_storage_options: ""
  docker_engine_storage_devs: []
  docker_engine_storage_vg: ""
  docker_engine_storage_root_size: "8G"
  docker_engine_storage_data_size: "40%FREE"
  docker_engine_storage_min_data_size: "2G"
  docker_engine_storage_chunk_size: "512K"
  docker_engine_storage_growpart: false
  docker_engine_storage_auto_exetend_pool: true
  docker_engine_storage_autoextend_threshold: 60
  docker_engine_storage_autoextend_percent: 20
  docker_engine_storage_device_wait_timeout: 60
  docker_engine_storage_wipe_signatures: false  
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
$ cd docker_engine/test
$ ansible-playbook main.yml
```

License
-------

Not defined.

Author Information
------------------

- Juan Antonio Valiño García (<juanval@edu.xunta.es>). Amtega - Xunta de Galicia
