Role Name
=========

Server preparation

Requirements
------------

This role configure deploy user and SSH params for Debian server

Role Variables
--------------

vault_ansible_user: root
vault_ansible_password: rootpassword
vault_deploy_user_name: deploy
vault_deploy_user_password: deployuserpassword

Dependencies
------------

This role does not have any dependencies

Example
-------

You can run this playbook with make

```
make create-deploy-user
```

For pass any inventory you can pass as parameters

```
make create-deploy-user INVENTORY=inventory.cfg
```

License
-------

GPLv3

Author Information
------------------

Maxim Ishchenko <m.g.ishchenko@yandex.ru>
