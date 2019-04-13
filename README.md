Role Name
=========

Ansible role for Openstack Designate service. In this role you can install designate service and configure it with openstack services.

Requirements
------------

Running Openstack and external DNS (Bind9) or use controller as main DNS.

Role Variables
--------------

The following variables must adapt based on your setup:

* osp_ctl_ip: 192.168.1.9

* bind_server: 192.168.1.6

* mysql_root_password: rhlab123

* designate_user_password: designate

* designate_db_user: designate

* designate_db: designate

* designate_osp_password: designate

Dependencies
------------

A running bind service, there is a bind role for this purpose.



Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: osp
      become: true
      remote_user: ayaseen
      gather_facts: yes
      roles:
        - designate

