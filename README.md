resolv_conf
===========

[![Build Status](https://travis-ci.org/kbrebanov/ansible-resolv_conf.svg?branch=master)](https://travis-ci.org/kbrebanov/ansible-resolv_conf)

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
```yaml
- hosts: all
  roles:
    - kbrebanov.resolv_conf
```

Configure /etc/resolv.conf file specifying nameservers and a search domain
```yaml
- hosts: all
  vars:
    resolv_conf_nameservers:
      - 8.8.4.4
      - 8.8.8.8
    resolv_conf_search_domains:
      - example.com
  roles:
    - kbrebanov.resolv_conf
```

License
-------

BSD

Author Information
------------------

Kevin Brebanov
