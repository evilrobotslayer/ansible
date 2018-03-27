Role Name
========

This role is designed to scan the designated hosts for filesystems with less than some threshold of remaining capacity.  In the case that the '/boot' filesystem is running below the threshold it will also attempt to remove old kernels that may be lying around.

Requirements
------------

This role requires:
Ansible 
Debian/Ubuntu or Redhat/CentOS based linux distribution

Role Variables
--------------

The variables that can be passed to this role and a brief description about
them are as follows:

    # Alert when filesystems have less than this percentage of free space
    capacity_threshold: 20

    # Always purge '/boot' filesystem if set "True" (will not override nopurge=True)
    purge_boot: False

    # Never purge the '/boot' filesystem (takes precedence over purge_boot=True)
    nopurge: False

    # Alert settings
    send_alerts: True
    alert_email: "user@email.com"

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
-------------------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

George M. Grindlinger
