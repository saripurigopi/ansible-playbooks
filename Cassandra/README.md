Setup Cassandra using Ansible
=============================

The playbooks are used to setup Apache Cassandra cluster on CentOS/RedHat.

Requirements
------------

Need to install the following packages.
 - Java8u162
 - Python-2.7.14 # *_skipped for now._*

Prerequisite playbook will takecare of installing these packages.

Usage
-----

You can run the playbook as listed below, either you can setup ssh keys for login or use ssh password.

```
ansible-playbook -vvv -i inventory -e ansible_python_interpreter=/usr/bin/python -e ansible_ssh_pass=<remote_user_password> setup-cassandra.yml
```


License
-------

BSD

Author Information
------------------

GopiKrishna Saripuri <GSaripuri@eplus.com>
