resolv_conf
===========

Configures /etc/resolv.conf file

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

| Name                       | Default                  | Description                     |
|----------------------------|--------------------------|---------------------------------|
| resolv_conf_nameservers    | ['8.8.8.8']              | List of nameserver IP addresses |
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
