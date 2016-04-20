resolv_conf
===========

[![Ansible Role](https://img.shields.io/ansible/role/3389.svg)](https://galaxy.ansible.com/list#/roles/3389)

Configures /etc/resolv.conf file

Requirements
------------

This role requires Ansible 1.9 or higher.

Role Variables
--------------

| Name                       | Default                  | Description                     |
|:---------------------------|:-------------------------|:--------------------------------|
| resolv_conf_nameservers    | ['8.8.8.8', '8.8.4.4']   | List of nameserver IP addresses |
| resolv_conf_search_domains | ["{{ ansible_domain }}"] | List of search domains          |

Dependencies
------------

None

Example Playbook
----------------

Configure /etc/resolv.conf file with default values
```
- hosts: all
  roles:
    - { role: kbrebanov.resolv_conf }
```

Configure /etc/resolv.conf file specifying nameservers and a search domain
```
- hosts: all
  roles:
    - { role: kbrebanov.resolv_conf, resolv_conf_nameservers: ['8.8.4.4', '8.8.8.8'], resolv_conf_search_domains: ['example.com'] }
```

License
-------

BSD

Author Information
------------------

Kevin Brebanov
