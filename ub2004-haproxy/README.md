ub2004-haproxy
=========

Installs haproxy & configures certbot for Let's Encrypt with intent to use the server as a primary SSL terminator.

Requirements
------------

Cloudflare DNS

Role Variables
--------------

##### ```site: 'example.com'```
The site variable will be the "wildcard" domain served. For example, this site would handle example.com, site1.example.com, site2.example.com, etc.

##### ```email: 'administrator@example.com'```
The email variable handles both the Let's Encrypt registration as well as the email associated with your Cloudflare account. If this is different for you you'll need to update one of templates/cloudflare, or tasks/main.yml

##### ```cloudflare_api_key: 'SECRET_KEY'```
This is your global API key for cloudflare. The ```python3-certbot-dns-cloudflare``` package in Ubuntu 20.04 does not yet support API tokens, you'll need to provide the Global API Key found [HERE](https://dash.cloudflare.com/profile/api-tokens). Hopefully this will change in Ubuntu 22.04

Example Playbook
----------------

    - hosts: haproxy-server
      become: yes
      vars:
        site: 'example.com'
        email: 'administrator@example.com'
        cloudflare_api_key: 'SECRET_KEY'
      roles:
        - ub2004-haproxy

License
-------

MIT

Author Information
------------------

Lyndon Lapierre  
https://t.me/ljlapierre  
https://github.com/ljlapierre
