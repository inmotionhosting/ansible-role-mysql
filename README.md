inmotionhosting.mysql
=======

Modular Ansible Role for deploying and configuring MySQL/MariaDB

[![Build Status](https://travis-ci.org/inmotionhosting/ansible-role-mysql.png?branch=master)](https://travis-ci.org/inmotionhosting/ansible-role-mysql)

Requirements
------------

* CentOS 7.x or later
* Debian 8 or later
* Ubuntu 16.04.x LTS or later

Role Variables
--------------
In this role, we load the defaults and then modify them as needed to
support other platforms.

### Defaults
This role uses [defaults/main.yml](defaults/main.yml) to declare
"global" variables using CentOS 7.x as our base.  This allows defining
a core set of variables that can be trivially modified.

### Vars
This role uses [vars/](vars/) to handle variances between operating
systems and their derivatives, which are loaded and sanitized in
[tasks/facts.yml](tasks/facts.yml), including handling any errata.

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: www
      roles:
         - role: inmotionhosting.mysql

License
-------

GPLv3

Author Information
------------------

InMotion Hosting
