Role Name
=========

Installs & upgrades [Bookstack](https://www.bookstackapp.com), along with required software such as a LAMP stack & PHP Composer

Requirements
------------

If providing UFW IP, ensure the UFW firewall is enabled prior to running the role

Role Variables
--------------

##### ```site: 'bookstack.example.com'```
The site variable configures the FQDN into the Apache site config

##### ```wkhtmltopdf_deburl: 'https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6-1/wkhtmltox_0.12.6-1.focal_amd64.deb'```
*Optional*  
See Bookstack's documentation on [PDF Rendering](https://www.bookstackapp.com/docs/admin/pdf-rendering/)  
This URL link installs the deb package for wkhtmltopdf

##### ```ufw_fromip: '192.168.1.100'```
*Optional*  
If you're using UFW firewall in Ubuntu, you can provide an IP or subnet reference to allow to talk to Bookstack. If using a load balancer, you may want to restrict incoming traffic to that.

Example Playbook
----------------

    - hosts: bookstack-server
      become: yes
      vars:
        site: 'bookstack.example.com'
        wkhtmltopdf_deburl: 'https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6-1/wkhtmltox_0.12.6-1.focal_amd64.deb'
        ufw_fromip: '192.168.1.100'
      roles:
        - ub2004-bookstack

License
-------

MIT

Author Information
------------------

Lyndon Lapierre  
https://t.me/ljlapierre  
https://linkedin.com/in/lyndonlapierre  
https://github.com/ljlapierre
