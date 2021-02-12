# odoo-devops

here will added my ansible playbooks for odoo developement enviorment 

Ansible Roles lists
=========

To configure latest services from list bellow
  - {role: common, tags: common }
  - {role: fail2ban, tags: fail2ban}
  - {role: rclone, tags: rclone}
  - {role: users, tags: users}
  - {role: sudoer, tags: sudoer}
  - {role: ufw, tags: ufw}
  - {role: odoo_certbot, tags: odoo_certbot}
  - {role: odoo_backup, tags: odoo_backup}
  - {role: wkhtmltopdf, tags: wkhtmltopdf}

Requirements
------------
None.

Role Variables
--------------
Remote user
1. vagrant
2. ec2-user
3. root

```
remote_user: root
```

Dependencies
------------

None.

Example Playbook
----------------


    $ cat inventory
    [servers]
    172.10.10.1
    [local]
    localhost ansible_ssh_hostname=127.0.0.1 ansible_ssh_user=vagrant


   **to run uncomment from above roles and pass tags to it
    $ ansible-playbook -i inventory site.yml --tags common

License
-------

MIT

Author Information
------------------

Algazali Hamid ([@gyzi](https://github.com/gyzi))
