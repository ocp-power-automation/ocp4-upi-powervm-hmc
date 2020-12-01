update-inventory: add cluster nodes to inventory
=========

This module will add the cluster node to inventory.

Requirements
------------

The vars.yaml files contains all cluster node definitions.

Role Variables
--------------

None

Dependencies
------------

 None

Example Playbook
----------------
```
    - name: Update inventory to have all hosts defined in vars.yaml
      hosts: bastion
      gather_facts: no
      any_errors_fatal: true
      roles:
      - update-inventory
```
License
-------

See LICENCE.txt

