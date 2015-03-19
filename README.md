resolv_conf
===========

Configures /etc/resolv.conf file

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

Dependencies
------------

Example Playbook
----------------

1) Configure /etc/resolv.conf file

    - hosts: all
      roles:
         - { role: resolv_conf }

License
-------

BSD

Author Information
------------------

Kevin Brebanov
