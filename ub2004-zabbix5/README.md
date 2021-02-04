ub2004-bookstack
=========

Install Zabbix 5.0 LTS Server

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

    - hosts: zabbix5-server
      become: yes
      vars:
        ufw_fromip: '192.168.1.100'
      roles:
        - ub2004-zabbix5

License
-------

MIT

Author Information
------------------

Lyndon Lapierre  
[Telegram](https://t.me/ljlapierre) | [LinkedIn](https://linkedin.com/in/lyndonlapierre) | [Github](https://github.com/ljlapierre)
