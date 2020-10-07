Role Name
=========

This role installs a host file based (DNS) blocking based upon [energized](https://energized.pro/). The original hosts file is backed up to `/etc/hosts.original` and can be restored by running the role with `hosts_pack: none` again.

Have a look at [packs](https://block.energized.pro/) for an overview of available packs and their features.

Requirements
------------

- Sudo permission

ansible-role-system
--------------

| Variable| Description | default |
|---------|-------------|---------|
| hosts_pack | which hosts pack to use from energized | spark |
| thinkpad | Thinkpad specific settings|  |
| user | to add to plugdev group for ergodox rule | |

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
        thinkpad: true
        user: michael
  roles:
    - ansible-role-system
```

License
-------

MIT
