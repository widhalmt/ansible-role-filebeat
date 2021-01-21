Filebeat
=========

[![CI](https://github.com/widhalmt/ansible-role-ansible/workflows/Molecule%20Test/badge.svg?event=push)](https://github.com/widhalmt/ansible-role-filebeat/workflows/Molecule%20Test/badge.svg)

This role installs and configures Filebeat.

*WARNING*: This is a very, very early prototype only usable for a very specific environment. **DO NOT USE IN PRODUCTION**

Requirements
------------

You need to have Filebeat available in your software repositories. We provide a role for just that but if you have other ways of managing software, just make sure it's available. Alternatively you can install Filebeat yourself.

Role Variables
--------------

* **filebeat_syslog_udp**: Use UDP Syslog input (Default: `false`)
* **filebeat_syslog_udp_port**: Port of UDP Syslog input (Default: `514`)
* **filebeat_syslog_tcp**: Use TCP Syslog input (Default: `false`)
* **filebeat_syslog_tcp_port**: Port of TCP Syslog input (Default: `514`)
* **filebeat_log_input**: Enable Logfile reading (Default: `true`)
* **filebeat_log_inputs**: Logfiles to read (Default: see below)

Default of `filebeat_log_inputs`
```
  messages:
    name: messages
    paths:
      - /var/log/messages
```

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
