Role Name: osp-servers
=========

This role performs the creation of Openstack instances. It will create the intances and attached to a network, then a floating IP will be created and assigned to every instance and the role will wait until the instance is up.

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

An example to use this role calling all the tasks with "apps" in the tags section:

```
    - hosts: servers
      vars_files:
        - vars/three-tier-app/instances.yml
      roles:
        - osp-servers
```

License
-------

BSD

Author Information
------------------

Contact Mail: asalgado@redhat.com
