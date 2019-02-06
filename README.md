Ansible Role: Apache SSL Redirect
=========

This Role installs Apache Web Server on a PC and redirect all requests from HTTP to HTTPS. The certificate is not valid, you should find one who does work. Once you have it, you should go to 

    ansible-apache-ssl-redirect/files/default-ssl.conf

and change the following line

    SSLCertificateFile	/etc/apache2/apache.pem

for the route to your ssl certificate is located.

Requirements
------------

It needs no extra roles.

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

    apache_server_root: /etc/apache2
    apache_conf_path: /etc/apache2
        
    __apache_packages:
    	- apache2
    	- apache2-utils


Example Playbook
----------------

    - hosts: localhost
      remote_user: root
      roles:
    	- ansible-apache-ssl-redirect

License
-------

BSD

Author Information
------------------

This role was created in 2019 by Jibsan Joel Rosa Toirac.
