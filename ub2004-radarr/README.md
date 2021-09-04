Role Name
=========

This role installs, configures & updates Radarr on Ubuntu 20.04

Requirements
------------

If providing UFW IP, ensure the UFW firewall is enabled prior to running the role

Role Variables
--------------

##### ```ufw_fromip: '192.168.1.100'```
*Optional*  
If you're using UFW firewall in Ubuntu, you can provide an IP or subnet reference to allow to talk to Bookstack. If using a load balancer, you may want to restrict incoming traffic to that.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: radarr-server
      become: yes
      vars:
        ufw_fromip: '192.168.1.100'
      roles:
        - ub2004-radarr

License
-------

MIT

Author Information
------------------

Lyndon Lapierre  
[Telegram](https://t.me/ljlapierre) | [LinkedIn](https://linkedin.com/in/lyndonlapierre) | [Github](https://github.com/ljlapierre)
