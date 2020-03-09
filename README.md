inmotion.ultrastack_mysql
=========

Modular Ansible Role for deploying and configuring MySQL/MariaDB

[![Build Status](https://travis-ci.org/inmotionhosting/inmotion.mysql.png?branch=master)](https://travis-ci.org/inmotionhosting/inmotion.mysql)

Requirements
------------

* CentOS 7.x or later
* Debian 8 or later
* Ubuntu 16.04 LTS or later

Role Variables
--------------

### Defaults
| Variable | Description |
| -------- | ----------- |
| mysql_slow_query_log_enabled | Whether logging slow queries should occur. <br><br>Default: `true`
| mysql_enabled_on_startup | Whether the MuSQL service should start on boot. <br><br>Default: `true`
| mysql_root_password_update | Whether the MySQL root password should be updated. <br><br>Default: `false`
| mysql_user_password_update | Whether the MySQL user password should be updated. <br><br>Default: `false`

### Vars
| Variable | Description |
| -------- | ----------- |
| mysql_config_file | Location of MySQL config file
| mysql_config_include_dir | Location of MySQL config directory for includes
| mysql_daemon | The name of the mysql daemon
| mysql_packages | The packages to install that provide MySQL
| mysql_log_error | Location of MySQL error log
| mysql_log_file_group | The name of MySQL logging group
| mysql_pid_file | Location of the MySQL PID file
| mysql_slow_query_log_file | Location of the MySQL slow query log file
| mysql_supports_innodb_large_prefix | Whether MySQL supports InnoDB index key prefixes longer than 767 bytes (up to 3072 bytes)
| mysql_syslog_tag | The name of the MySQL syslog tag
| mysql_root_home | Directory of the root user's home
| mysql_root_username | The name of the MySQL root user

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: www
      roles:
         - role: inmotion.mysql

License
-------

GPLv3

Author Information
------------------

InMotion Hosting
