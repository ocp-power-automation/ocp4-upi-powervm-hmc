bootup-nodes: boot up the cluster node with bootp
=========

This module will boot up all cluster node with `lpar_netboot` on HMC to bootp to install RHCOS to disk and reboot from RHCOS to run ignition to setup the RHCOS.

Requirements
------------

 - Keyless ssh to HMC from bastion


Role Variables
--------------

None

Dependencies
------------

None

Example Playbook
----------------

    - name: Net boot all cluster nodes
      hosts: bastion
      gather_facts: no
      any_errors_fatal: true
      roles:
      - bootup-nodes

License
-------

See LICENCE.txt

