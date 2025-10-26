ub2404-bookstack
=========

Installs & upgrades [Bookstack](https://www.bookstackapp.com), along with required software such as a LAMP stack & PHP Composer

Requirements
------------

If providing UFW IP, ensure the UFW firewall is enabled prior to running the role

Role Variables
--------------

##### ```site: 'bookstack.example.com'```
The site variable configures the FQDN into the Apache site config

##### ```ufw_fromip: '192.168.1.100'```
*Optional*  
If you're using UFW firewall in Ubuntu, you can provide an IP or subnet reference to allow to talk to Bookstack. If using a load balancer, you may want to restrict incoming traffic to that.

Example Playbook
----------------

    - hosts: bookstack-server
      become: yes
      vars:
        site: 'bookstack.example.com'
        ufw_fromip: '192.168.1.100'
      roles:
        - ub2404-bookstack

License
-------

MIT

Author Information
------------------

Lyndon Lapierre  
[LinkedIn](https://linkedin.com/in/lyndonlapierre) | [Github](https://github.com/ljlapierre)
