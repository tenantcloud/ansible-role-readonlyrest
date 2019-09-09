Ansible role for install and setup readonlyrest plugin for elasticsearch
=========

ReadOnlyRest ELK role. This role include in default terraform scenario for auto-deploy new server.
Plugin activate access to ELK Stack only with login/password.
Don't forget disable X-Pack's Security Module from both elasticsearch.yml and kibana.yml.
To download plugin visit https://readonlyrest.com/download/ and select in Product > Elasticsearch plugin (Free), chose ELK Stack version and enter email.
Place downloaded plugin on avaliable url, enter this url in variable url: "{{ ror_git }}" in you-playybok-name.yml:

-------

For manual installation this role:

```ansible-galaxy install tenantcloud.ansible_role_readonlyrest```

Add this role name to playbook and run:

```cd /tmp/.ansible/ && ansible-playbook playbook-name.yml```

