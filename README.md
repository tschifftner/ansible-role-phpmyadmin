# Ansible Role: phpMyAdmin

[![Build Status](https://travis-ci.org/tschifftner/ansible-role-phpmyadmin.svg)](https://travis-ci.org/tschifftner/ansible-role-phpmyadmin)

Installs phpMyAdmin on Debian/Ubuntu linux servers.

## Requirements

nginx and php5-fpm need to be installed.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

### Security

This phpMyAdmin installation is chrooted. Therefore please use ip address (i.e. 127.0.0.1) instead of hostnames!

```
mariadb_admin_home: '/root'
mariadb_admin_user: 'admin'
mariadb_admin_password: 'Set strong password here!'
```

## Dependencies

None.

## Example Playbook

    - hosts: server
      roles:
        - { role: tschifftner.phpmyadmin }

## Supported OS
Ansible          | Debian Jessie    | Ubuntu 14.04    | Ubuntu 12.04
:--------------: | :--------------: | :-------------: | :-------------: 
2.0              | Yes              | Yes             | Yes

## License

MIT / BSD

## Author Information

 - Tobias Schifftner, @tschifftner