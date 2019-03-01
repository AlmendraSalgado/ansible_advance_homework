Role Name: lb-tier
=========

This role performs the setup for load balancer services in the lb nodes in the three tier app environment. It will install the HAProxy packages, deploy the configuration file for haproxy service and start/enable the service.

Requirements
------------

The only requirement is to have access to the correct repositories to install the required packages.

Role Variables
--------------

The role has the next default variables:

| Defaults Variables | Description |
| ------------- | ------------- |
| HAPROXY_PACKAGES | HAProxy packages to install  |

Dependencies
------------

It doesn't have any role dependencies.

Example Playbook
----------------

An example to use this role calling all the tasks with "lbs" and "haproxy" in the tags section:

```
    - hosts: servers
      roles:
        - {name: lb-tier, tags: [lbs, haproxy]}
```

License
-------

BSD

Author Information
------------------

Contact Mail: asalgado@redhat.com
