ub2004-haproxy
=========

Installs haproxy & configures certbot for Let's Encrypt with intent to use the server as a primary SSL terminator.

Requirements
------------

Cloudflare DNS

Role Variables
--------------

site: 'example.com'
email: 'administrator@example.com'
cloudflare_api_key: 'SECRET_KEY'

- site: 'example.com'
The site variable will be the "wildcard" domain served. 

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

- hosts: int-proxy-01
  become: yes
  vars:
    site: 'example.com'
    email: 'administrator@example.com'
    cloudflare_api_key: 'SECRET_KEY'
  roles:
    - ub2004-haproxy

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:



    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

MIT

Author Information
------------------

Lyndon Lapierre  
https://t.me/ljlapierre  
https://www.ljlapierre.com  
https://github.com/ljlapierre
