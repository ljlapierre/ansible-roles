ub2004-firefly3
=========

Installs & upgrades [Firefly III](https://www.firefly-iii.org) to the latest stable release, along with required software such as a LAMP stack & PHP Composer

Requirements
------------

If providing UFW IP, ensure the UFW firewall is enabled prior to running the role

Role Variables
--------------

##### ```site: 'firefly3.example.com'```
The site variable configures the FQDN into the Apache site config

##### ```use_memcached: no```
*Optional*  
Setting this variable to yes installed memcached plugins for you. Defaults to no.

##### ```locales: 'en_US.UTF-8'```
*Optional*  
Ensures the listed locales are are available on the system. Can be a list of multiple items (see example playbook below). Defaults to en_US.UTF-8

##### ```ufw_fromip: '192.168.1.100'```
*Optional*  
If you're using UFW firewall in Ubuntu, you can provide an IP or subnet reference to allow to talk to Bookstack. If using a load balancer, you may want to restrict incoming traffic to that.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: firefly3-server
      become: yes
      vars:
        site: 'firefly3.example.com'
        use_memcached: yes
        locales:
          - 'en_CA.UTF-8'
          - 'en_US.UTF-8'
        ufw_fromip: '192.168.1.100'
      roles:
         - ub2004-firefly3

License
-------

MIT

Author Information
------------------

Lyndon Lapierre  
[Telegram](https://t.me/ljlapierre) | [LinkedIn](https://linkedin.com/in/lyndonlapierre) | [Github](https://github.com/ljlapierre)
