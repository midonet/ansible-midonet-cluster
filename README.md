[![Build Status](https://travis-ci.org/abelboldu/ansible-midonet-cluster.svg?branch=master)](https://travis-ci.org/abelboldu/ansible-midonet-cluster)


midonet-cluster
===============

Ansible role for the Midonet cluster.
The MidoNet Cluster provides the REST API endpoint, and also hosts a number of management services such as VxLAN Gateway Controller.

Requirements
------------

Ubuntu or RedHat/CentOS

Role Variables
--------------

* Required:

`zookeeper_hosts` should be a dictionary or group in hosts inventory with all zookeeper members.
`cassandra_hosts` should be a dictionary or group in hosts inventory with all cassandra members.

* Not Required:




Dependencies
------------

Midonet repositories ( abelboldu.midonet-repos )


Example Playbook
----------------

```
- hosts: controller
    roles:
      - role: abelboldu.midonet-agent
        zookeeper_hosts: '{{ groups["zookeeper"] }}'
        cassandra_hosts: '{{ groups["cassandra"] }}'
        midonet_password: 'midonet'
```



License
-------

Apache 2.0
