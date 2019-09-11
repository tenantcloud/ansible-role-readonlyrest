tenantcloud.ansible_role_readonlyrest
=========

Ansible role for install and setup ReadOnlyRest plugin. This role include in default terraform scenario for auto-deploy new server.

Requirements
------------

ELK Stack, Elastalert

Role Variables
--------------

ror_git: https://s3.amazonaws.com/software/readonlyrest-1.18.4_es6.8.2.zip
Url for download readonlyrest archive from S3 bucket

var.username
var.password
This vars include Usernames and passwords to generate block for each user in config file.

Dependencies
------------

  - geerlingguy.java
  - geerlingguy.elasticsearch
  - geerlingguy.kibana
  - geerlingguy.logstash
  - tenantcloud.ansible_role_elastalert
  - tenantcloud.ansible_role_auth_elk

Example Playbook
----------------

```yaml
  - hosts: localhost
    vars:
      ea_dir: elastalert
      creds:
        - {username: "${user1}",  password: "${pass1}"}
    become: yes
    roles:
      - tenantcloud.ansible_role_readonlyrest
```

License
-------

BSD

Author Information
------------------

TenantCloud DevOps Team
