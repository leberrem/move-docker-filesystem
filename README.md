Role Name
=========

Move docker filesystem.

Requirements
------------

docker daemon.

Role Variables
--------------

You must set a list of groups and users with options.

sample:

```yaml
from_folder: "var/lib/docker"
to_folder: "/data/docker"
```

Dependencies
------------

No dependencies.

Example Playbook
----------------

```yaml
- hosts: servers
  become : yes
  tasks:
    - name: Move docker filesystem
      include_role:
        name: move-docker-filesystem
      vars:
        from_folder: "/var/lib/docker"
        to_folder: "/data/docker"
```

License
-------

GPLv3

Author Information
------------------

Mikael LE BERRE
