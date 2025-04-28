Role Name
=========

Prepares system for an installation of [Pi-hole](https://pi-hole.net), along with the cloudflared backend required for DoH.

Requirements
------------

Ensure the UFW firewall is enabled prior to running the role

Role Variables
--------------

##### ```dns_test_address: 'google.ca'```
The DNS site to be watched by the cloudflared service. I recommend a site with a short TTL, mine is configured for two minutes

##### ```ufw_fromip: '192.168.1.100'```
Provide the IP or subnet allowed to talk to the pi-hole web server. If using a load balancer, you may want to restrict incoming traffic to that.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
 
    - hosts: pihole-server
      become: yes
      vars:
        dns_test_address: 'dohtest.ljlapierre.com'
        ufw_fromip: '192.168.1.203'
      roles:
        - ub2204-pihole

License
-------

MIT

Author Information
------------------

Lyndon Lapierre  
[LinkedIn](https://linkedin.com/in/lyndonlapierre) | [Github](https://github.com/ljlapierre)
