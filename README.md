extend-disk
=========

name: ansible-role-extend-disk
The purpose of this role is to extend the root file system by added a new partition from available space on the disk extended.
This is mainly to help the libvirt automation.

Requirements
------------

Disk thats already been extended at the hypervisor layer.

Role Variables
--------------

Most variables required for this role to run are currently set in the defaults directory of the role and need to be overriden if not using vda and rhel vg.


Example Playbook
----------------

- name: Extend disk 
  hosts: localhost  
  become: true

  tasks:
    - name: "Include the extend disk role"
      include_role:
        name: ../roles/ansible-role-extend-disk


License
-------

MIT

