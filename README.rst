ansible-abbr
############

An ansible role to roll out the free, open-source and privacy conscious URL
shortener abbr_ on your server!

Requirements
============

This role was written for Arch Linux and nginx, and does not include SSL certificate
actions. If your requirements are different, I'll gladly accept pull requests adding
them to this role.

Role Variables
==============

These are variables this role will read::

    abbr_domain: 'localhost'
    abbr_name_length: 5  # default length of shortened links
    abbr_gunicorn_sock_dir: '/var/run/nginx'
    abbr_gunicorn_sock_path: '{{ abbr_gunicorn_sock_dir }}/gunicorn_abbr.sock'
    abbr_gunicorn_workers: 3

    abbr_user: 'abbr'
    abbr_home: '/home/abbr'
    abbr_source_dir: '{{ abbr_home }}/src'
    abbr_log_dir: '/var/log/nginx'

    abbr_cert_path: '/etc/ssl/letsencrypt/certs/{{ abbr_domain }}/'
    abbr_cert_name: 'fullchain.pem'
    abbr_key_name: 'privkey.pem'

License
=======

BSD

Author
======

rixx

.. _abbr: https://github.com/rixx/abbr
