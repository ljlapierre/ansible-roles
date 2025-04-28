ub2004-ncpa 
=========

Installs & customizes the Nagios NCPA agent for use on an Ubuntu system

Requirements
------------

If providing UFW IP, ensure the UFW firewall is enabled prior to running the role
If you're going to use the Sanoid plugins you should have the sanoid package installed & config file created for your ZFS pools.
If you're going to use apcupsd for UPS monitoring you should have the apcupsd package installed & configured

Role Variables
--------------

##### ```ncpa_community_string: 'secret_community_string'```
The site variable configures the community string for authenticating the NCPA client

##### ```ufw_fromip: '192.168.1.100'```
*Optional*  
If you're using UFW firewall in Ubuntu, you can provide an IP or subnet reference to allow to talk to Tautulli. If using a load balancer, you may want to restrict incoming traffic to that.

Example Playbook
----------------

    - hosts: monitored-server
      become: yes
      vars:
        ufw_ncpa: '192.168.1.100'
        ncpa_community_string: 'secret_community_string'
      roles:
        - ub2004-ncpa

License
-------

MIT

Author Information
------------------

Lyndon Lapierre  
[LinkedIn](https://linkedin.com/in/lyndonlapierre) | [Github](https://github.com/ljlapierre)

The check_apcupsd plugin was originally written by Martin Toft, original plugin is available on [Martin's website](http://martintoft.dk/?p=check_apcupsd).  
A slightly outdated version is also available from the [Nagios Exchange](https://exchange.nagios.org/directory/Plugins/Hardware/UPS/APC/check_apcupsd)