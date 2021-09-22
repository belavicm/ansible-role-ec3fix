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
# Send mail from front
sendemail: False
# Emailsmtp
emailsmtp: smtp3.srce.hr
# Project name
project: Srce-HTC
# Home prefix
homeprefix: /storage
```

Example Playbook
----------------

This an example of how to install a SGE cluster with three nodes:
```
- hosts: server
  roles:
  - { role: 'srce.ec3-cloud-users', sge_type_of_node: 'front', sendemail: False, project: 'Srce-HTC', homeprefix: '/storage'}

- hosts: server
  roles:
  - { role: 'srce.ec3-cloud-users', sge_type_of_node: 'wn', sendemail: False, project: 'Srce-HTC', homeprefix: '/storage'}
```
