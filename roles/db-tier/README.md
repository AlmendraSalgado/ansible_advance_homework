Role Name: db-tier
=========

This role performs the setup for db services in the db nodes in the three tier app environment. It will install postgresql packages, check if the database was previously initialized, initialize the db if It wasn't do it before and start/enable the service.

Requirements
------------

The only requirement is to have access to the correct repositories to install the required packages.

Role Variables
--------------

The role has the next default variables:

| Defaults Variables | Description |
| ------------- | ------------- |
| POSTGRESQL_PACKAGES | PostgreSQL packages to install  |

Dependencies
------------

It doesn't have any role dependencies.

Example Playbook
----------------

An example to use this role calling all the tasks with "dbs" and "postgres" in the tags section:

```
    - hosts: servers
      roles:
        - {name: db-tier, tags: [dbs, postgres]}
```

License
-------

BSD

Author Information
------------------

Contact Mail: asalgado@redhat.com
