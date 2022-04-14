## Features
Initial setting for AlmaLinux 8

* yum update
* install module
* set timezone/locale/keymap
* set hostname
* create user for operation
* disable SELinux
* disable IPv6
* set module enable on systemd
* set module disable on systemd
* set snmp (snmpd.conf)
* set ntp (chrony.conf)
* restart host

## Require
Ansible on AlmaLinux 8

## Install
Set the following variables in **group_vars/Linux_servers.yml**
| variable| explanation |
| ------ | ------ |
| local_timezone | local timezone|
| local_locale | local locale |
| locale_keymap |local keymap  |
| linux_hostname | hostname |
| user_newusers| username,userpassword and user group |
| install_packages_list | install package list |
| enabled_packages_list| enable module list |
| disabled_packages_list | disable module list |
| snmp_community_name | snmp community name in snmpd.conf |
| ntp_time_server | [ntp server name in chrony.conf |

run ansible playbook
```sh
ansible-playbook -i inventory.ini almalinux-base-setting.yml
```