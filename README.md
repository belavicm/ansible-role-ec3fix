[![License](https://img.shields.io/badge/license-Apache%202-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0)

Ec3 Cloud Users Role
=======================

Install [ec3-cloud-users](https://github.com/vrdel/ec3-cloud-users).
Recipe to be used by [EC3](http://servproject.i3m.upv.es/ec3/).

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows.
```
# Type of node to install: front or wn
sge_type_of_node: front
# Prefix to set to the SGE working nodes
sge_vnode_prefix: wn
# Number of CPUs of the WNs
sge_wn_cpus: 1
# Default ssh user
sge_ssh_user: grycap
# Number of Maximum nodes
max_number_of_nodes: 3
```

Example Playbook
----------------

This an example of how to install a SGE cluster with three nodes:
```
- hosts: server
  roles:
  - { role: 'grycap.ec3-cloud-users', sge_type_of_node: 'front' }
```
