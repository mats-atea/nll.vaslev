Role Name
=========

Role to move, snap, upgrade and reboot VAS servers

Requirements
------------

Need pyVmomi installed. Do this with the "pip-3 install pyVmomi" command

Role Variables
--------------

set all the vcenter-variables in defaults/main.yml
These are needed to run the task.

the inventory file also need variables for which host to run on for the different datacenters (see invontory in test):
vas-server1 vcenter_dest_a=esxi01 vcenter_dest_b=esxi02
vas-server2 vcenter_dest_a=esxi03 vcenter_dest_b=esxi04

Dependencies
------------

- community.vmware

Example Playbook
----------------

Playbook requires the "hall" variable to be set in either the roles or with a prompt (see examplei in test)

    - hosts: vasservers
      roles:
         - { role: nll.vaslev, hall: b }

License
-------

BSD

