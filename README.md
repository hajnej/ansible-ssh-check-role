ansible-ssh-check-role
=========

This role is used for checking SSH access through default SSH port or preconfigured port in inventory.

Requirements
------------

There is not any prerequisities for this role.

Role Variables
--------------

Only ansible internal variables are used. `ansible_port` contains configured prt number which defaults to 22 in case it is not preconfigured.

Dependencies
------------

There are not any direct dependencies. This role is used by other ansible roles to check SSH access. Discovered SSH port number is saved into `sshd_port` fact variable.

Example Playbook
----------------

This role has to be invoked with `gather_facts: False` parameter. Facts are gahered in the end of this role.

    - hosts: "all"
      gather_facts: False
      roles:
         - "ansible-ssh-check-role"

License
-------

BSD

Author Information
------------------

Jakub Slatinsky, slatinskyj@gmail.com
