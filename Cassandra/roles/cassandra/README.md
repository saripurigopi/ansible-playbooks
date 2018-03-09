Cassandra
=========

Nodes which are part of cassandra cluster.

Requirements
------------

Need to install the following packages.
 - Java8u162
 - Python-2.7.14

Prerequisite playbook will takecare of installing these packages.

Role Variables
--------------

Need to update the variables in vars/main.yml file. The initial support 

```
CASSANDRA_VERSION: 311x # Available options 21x, 22x, 30x, 311x
CASSANDRA_CLUSTER_NAME: eplus
CASSANDRA_CLUSTER_SEEDS: "10.32.68.40,10.32.68.41,10.32.68.42"
CASSANDRA_STORAGE_PORT: 7000
LISTEN_ADDRESS: {{ inventory_hostname }} 
LISTEN_INTERFACE: ens160
NATIVE_TRANSPORT_PORT: 9042
CASSANDRA_SSL_STORAGE_PORT: 7001

# location of directories
DATA_FILE_DIRECTORIES: /var/lib/cassandra/data
COMMITLOG_DIRECTORY: /var/lib/cassandra/commitlog
SAVED_CACHES_DIRECTORY:
HINTS_DIRECTORY:

# JVM options
JVM_OPTS:

# Logging
LOG_LEVEL: INFO
```

Dependencies
------------

None

Example Playbook
----------------

You can include this role in your playbooks as lister below.

    - hosts: servers
      roles:
         - cassandra

License
-------

BSD

Author Information
------------------

GopiKrishna Saripuri<GSaripuri@eplus.com>
