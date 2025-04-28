ub2004-jellyfin
=========

Installs jellyfin via apt repository, as well as Intel driver packages, and opens the firewall to a load balancer if defined.

Requirements
------------

- Intel Graphics
- UFW installed and enabled

If providing UFW IP, ensure the UFW firewall is enabled prior to running the role

Role Variables
--------------

##### ```ufw_fromip: '192.168.1.100'```
*Optional*  
If you're using UFW firewall in Ubuntu, you can provide an IP or subnet reference to allow to talk to Jellyfin. If using a load balancer, you may want to restrict incoming traffic to that.

License
-------

MIT

Author Information
------------------

Lyndon Lapierre  
[LinkedIn](https://linkedin.com/in/lyndonlapierre) | [Github](https://github.com/ljlapierre)
