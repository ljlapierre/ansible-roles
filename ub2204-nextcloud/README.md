ub2204-nextcloud
=========

This role installs and configures Nextcloud on Ubuntu 22.04 with MariaDB.
Use the ```migrate``` tag to run the role without downloading and installing a new version of Nextcloud.

Role Variables
--------------

##### ```site: 'cloud.example.com'```
The site variable will be configured in apache

##### ```ufw_fromip: '192.168.1.100'```
*Optional*  
If you're using UFW firewall in Ubuntu, you can provide an IP or subnet reference to allow to talk to Nextcloud. If using a load balancer, you may want to restrict incoming traffic to that.

##### ```apt_packages```
All apt packages to be installed from the Ubuntu repos

##### ```apache_modules```
All apache2 modules to be enabled for Nextcloud

##### ```php_options```
A few sane defaults to configure in PHP. Update these as you see fit!

Example Playbook
----------------

    - hosts: nextcloud-server
      become: yes
      vars:
        site: 'cloud.example.com'
        ufw_fromip: '192.168.1.100'
      roles:
        - ub2204-nextcloud

License
-------

MIT

Author Information
------------------

Lyndon Lapierre  
[Telegram](https://t.me/ljlapierre) | [LinkedIn](https://linkedin.com/in/lyndonlapierre) | [Github](https://github.com/ljlapierre)
