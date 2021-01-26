
![Lint Ansible Roles](https://github.com/tenantcloud/ansible-role-readonlyrest/workflows/Lint%20Ansible%20Roles/badge.svg)

tenantcloud.readonlyrest
=========

Ansible role for install and setup ReadOnlyRest plugin. This role include in default terraform scenario for auto-deploy new server.

Requirements
------------

ELK Stack, Elastalert

Role Variables
--------------

ror_git: https://tenantcloud.s3-us-west-2.amazonaws.com/software/readonlyrest-1.19.0_es7.5.2.zip
Url for download readonlyrest archive from S3 bucket

var.username
var.password
This vars include Usernames and passwords to generate block for each user in config file.

Dependencies
------------

  - geerlingguy.java
  - tenantcloud.elasticsearch
  - tenantcloud.kibana
  - tenantcloud.logstash
  - tenantcloud.elastalert
  - tenantcloud.auth_elk

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
      - tenantcloud.readonlyrest
```

License
-------

BSD

Author Information
------------------

TenantCloud DevOps Team
