Role Name
=========

This role installs a host file based (DNS) blocking based upon [energized](https://energized.pro/). The original hosts file is backed up to `/etc/hosts.original` and can be restored by running the role with `hosts_pack: none` again.

Have a look at [packs](https://block.energized.pro/) for an overview of available packs and their features.

Requirements
------------

- Sudo permission

Role Variables
--------------

| Variable| Description | default |
|---------|-------------|---------|
| hosts_pack | which hosts pack to use from energized | spark |

Dependencies
------------

No dependencies

Example Playbook
----------------

```
---
- name: Playbook
  hosts: localhost
  connection: local
    pre_tasks:
        hosts_pack: basic
  roles:
    - ansible-role-system
```

License
-------

MIT
