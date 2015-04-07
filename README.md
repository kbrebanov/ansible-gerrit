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
| gerrit_version   | 2.10.2                                                           | Gerrit version to install     |
| gerrit_sha256sum | 3e113342ad053af3997fdc5e361ee71f77f34efb72ed1a266600ed4aa80e7f6d | SHA 256 sum of Gerrit version |

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
