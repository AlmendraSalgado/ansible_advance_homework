Role Name: app-tier
=========

This role performs the setup for http services in the app nodes in the three tier app environment. It will install tomcat and httpd (if it is specified), create directory paths to deploy html templates and start/enable the services.

Requirements
------------

The only requirement is to have access to the correct repositories to install the required packages.

Role Variables
--------------

The role has the next default variables:

| Defaults Variables | Description |
| ------------- | ------------- |
| TOMCAT_PACKAGES | Tomcat packages to install  |
| APACHE_PACKAGES | Apache packages to install  |

TOMCAT_PACKAGES - Tomcat packages to install

APACHE_PACKAGES - Apache packages to install

Dependencies
------------

It doesn't have any role dependencies.

Example Playbook
----------------

An example to use this role calling all the tasks with "apps" in the tags section:

```
    - hosts: servers
      roles:
        - {name: app-tier, tags: [apps]}
```

License
-------

BSD

Author Information
------------------

Contact Mail: asalgado@redhat.com
