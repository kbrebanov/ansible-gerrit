gerrit
======

Installs Gerrit

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

| Name             | Default                                                          | Description                   |
|------------------|------------------------------------------------------------------|-------------------------------|
| gerrit_version   | 2.11                                                             | Gerrit version to install     |
| gerrit_sha256sum | 05c155c454f06c324e89863e6c6a9c814833c7caea7b38f6c9b360336b30b96d | SHA 256 sum of Gerrit version |

Dependencies
------------

- kbrebanov.java

Example Playbook
----------------

Install Gerrit
```
- hosts: all
  roles:
    - { role: kbrebanov.gerrit }
```

Install Gerrit specifying version
```
- hosts: all
  roles:
    - { role: kbrebanov.gerrit, gerrit_version: 2.9.3 gerrit_sha256sum: fad71b288ecaf3241ea11fecebb2d5be4cfbdfade3e2037d23b94cce3dd3bc48 }
```

License
-------

BSD

Author Information
------------------

Kevin Brebanov
