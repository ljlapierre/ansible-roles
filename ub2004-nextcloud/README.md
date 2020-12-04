ub2004-nextcloud
=========

This role installs and configures Nextcloud on Ubuntu 20.04 with MariaDB

Role Variables
--------------

##### ```site: 'cloud.example.com'```
The site variable will be configured in apache

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
      roles:
        - ub2004-nextcloud

License
-------

MIT

Author Information
------------------

Lyndon Lapierre  
https://t.me/ljlapierre  
https://linkedin.com/in/lyndonlapierre  
https://github.com/ljlapierre
