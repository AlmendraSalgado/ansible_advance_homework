Role Name: site-osp-delete
=========

This role performs a deletion of the given OSP instances.

Requirements
------------

It requires access to Openstack.

Also, the role requires a variable called "osp_servers".

Role Variables
--------------

The role requires the definition of the next variables:

| Variables | Description |
| ------------- | ------------- |
| osp_servers | List of instances to remove |

Dependencies
------------

It doesn't have any role dependencies.

Example Playbook
----------------

An example to use this role with a variables file:

```
    - hosts: servers
      vars_files:
        - vars/three-tier-app/instances.yml
      roles:
        - osp-instance-delete
```

License
-------

BSD

Author Information
------------------

Contact Mail: asalgado@redhat.com
