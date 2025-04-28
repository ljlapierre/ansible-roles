Role Name
=========

This role installs, configures & updates Bazarr on Ubuntu 20.04

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

##### ```ufw_fromip: '192.168.1.100'```
*Optional*  
If you're using UFW firewall in Ubuntu, you can provide an IP or subnet reference to allow to talk to Bazarr. If using a load balancer, you may want to restrict incoming traffic to that.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: bazarr-server
      become: yes
      vars:
        ufw_fromip: '192.168.1.100'
      roles:
        - ub2004-bazarr

License
-------

MIT

Author Information
------------------

Lyndon Lapierre  
[LinkedIn](https://linkedin.com/in/lyndonlapierre) | [Github](https://github.com/ljlapierre)
