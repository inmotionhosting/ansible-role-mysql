[![Build Status](https://travis-ci.org/inmotionhosting/ansible-role-mysql.png?branch=master)](https://travis-ci.org/inmotionhosting/ansible-role-mysql) [![GPL-3.0 License](https://img.shields.io/github/license/inmotionhosting/ansible-role-mysql.svg?color=blue)](https://github.com/inmotionhosting/ansible-role-mysql/blob/master/LICENSE) [![GitHub stars](https://img.shields.io/github/stars/inmotionhosting/ansible-role-mysql.svg)](https://github.com/inmotionhosting/ansible-role-mysql/stargazers)

# Ansible Role: MySQL

Modular Ansible Role for deploying and configuring MySQL/MariaDB

## Requirements

* CentOS 7.x or later
* Debian 9 or later
* Ubuntu 16.04 LTS or later

## Dependencies

None.

## Role Variables

Available variables are listed below with their default values (you can also see `defaults/main.yml`)

| Variable | Description |
| -------- | ----------- |
| mysql_daemon | Default: `mariadb`
| mysql_supports_innodb_large_prefix | Default: `true`
| mysql_root_home | Default: `/root`
| mysql_root_password_update | Default: `false`
| mysql_root_username | Default: `root`
| mysql_config_file | Default: `/etc/my.cnf`
| mysql_config_include_dir | Default: `/etc/my.cnf.d`
| mysql_pid_file | Default: `/var/run/mariadb/mariadb.pid`
| mysql_socket | Default: `true`
| mysql_socket_path | Default: `/var/lib/mysql/mysql.sock`
| mysql_log_dir | Default: `/var/log/`
| mysql_log_error | Default: `"{{ mysql_log_dir }}/mariadb/mariadb.log"`
| mysql_log_file_group | Default: `mysql`
| mysql_slow_query_log_enabled | Default: `true`
| mysql_slow_query_log_file | Default: `"{{ mysql_log_dir }}/mysql-slow.log"`
| mysql_syslog_tag | Default: `mariadb`
| mysql_packages | Default: `The MySQL packages to install`
| password_generate | Default: `"{{ lookup('password', '/dev/null length=15 chars=ascii_letters') }}"`

## Example Playbook

```yaml
- hosts: www
  roles:
     - role: inmotionhosting.mysql
```

## License

GPLv3

## Author Information

[InMotion Hosting](https://inmotionhosting.com)
