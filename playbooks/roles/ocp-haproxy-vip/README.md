bootup-nodes: boot up the cluster node with bootp
=========

This module will setup the haproxy with VIP using current ocp master nodes.

Requirements
------------

None


Role Variables
--------------

  - ocp_haproxy_vip: define the VIP for the haproxy

Dependencies
------------

None

Example Playbook
----------------
```
- name: configures haproxy/VIP inside OCP
  hosts: bastion
  gather_facts: no
  any_errors_fatal: true
  tasks:
    - include_role:
        name: ocp-haproxy-vip
      when: (ocp_haproxy_vip is defined) and (ocp_haproxy_vip | length > 0) 
```
License
-------

See LICENCE.txt

