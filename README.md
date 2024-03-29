ansible-role-user
=================

[![Build Status](https://travis-ci.org/cjsteel/ansible-role-users.svg?branch=master)](https://travis-ci.org/cjsteel/ansible-role-users)

Manage users for CentOS 7, Ubuntu 14.04 and Ubuntu 16.04

Requirements
------------

None

Role Variables
--------------

See defaults/main.yml

Dependencies
------------

None

Example Playbook
----------------

    - name: Test the User role for CentOS and Ubuntu systems
      hosts: user
      become: yes
      become_method: sudo
    
      vars:
        - user_list:
          - name: user01
            uid: 2001
          - name: user02
            sudoers: false
            ssh_key: ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACAQCsizUbyTe...w== your_email@example.com
    #       ssh_key: "{{lookup('file', '$HOME/.ssh/id_rsa.pub')}}"        
    
      roles:
        - ansible-role-user

License
-------

BSD

Author Information
------------------

Kevin Coakley (https://github.com/kevincoakley)

Modifications
-------------

Christopher Steel (https://github.com/cjsteel)
