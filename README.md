gerrit
======

Installs Gerrit

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

| Name                         | Default                                                          | Description                                                        |
|------------------------------|------------------------------------------------------------------|--------------------------------------------------------------------|
| gerrit_version               | 2.11                                                             | Gerrit version to install                                          |
| gerrit_sha256sum             | 05c155c454f06c324e89863e6c6a9c814833c7caea7b38f6c9b360336b30b96d | SHA 256 sum of Gerrit version                                      |
| gerrit_auth_type             | 'OPENID'                                                         | Type of user authentication                                        |
| gerrit_canonical_web_url     | 'http://localhost:8080/'                                         | The default URL for Gerrit                                         |
| gerrit_database_type         | 'h2'                                                             | Type of database server                                            |
| gerrit_database_db           | 'db/ReviewDB'                                                    | Database path (h2) or name (PostgreSQL, MySQL)                     |
| gerrit_database_username     | ''                                                               | Username to connect to the database server as                      |
| gerrit_database_password     | ''                                                               | Password to authenticate to the database server with               |
| gerrit_database_hostname     | 'localhost'                                                      | Hostname of the database server                                    |
| gerrit_httpd_listen_url      | 'http://*:8080/'                                                 | The URL the internal HTTP daemon should listen on                  |
| gerrit_sendemail_smtp_server | 'localhost'                                                      | Hostname (or IP address) of a SMTP server that will relay messages |
| gerrit_sshd_listen_address   | '*:29418'                                                        | The local addresses the internal SSHD daemon should listen on      |

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
