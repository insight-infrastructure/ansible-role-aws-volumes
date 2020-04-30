ansible-role-aws-volumes
========================

This role mounts ephemeral volumes on AWS instances. Takes input of instance type and resolves how many volumes to mount.  

**Note to users:** 
- This is an early WIP with aspirations to stay current with mapping volumes to available instance types
- It attempts to solve the problem with having to lookup the ephemeral volume mount locations by simply specifying an instance type 
- Further work will be done with RAID arrays 


Requirements
------------

Ansible version >2.6

Role Variables
--------------

```yaml
instance_type: i3.4xlarge # Maps to offical instance type naming 
```

Example Playbook
----------------

```yaml
---
- hosts: all
  roles:
    - role: ansible-role-aws-volumes

  vars:
    instance_type:
```
License
-------

MIT 

Author Information
------------------
Maintained by [insight-infrastructure](https://github.com/insight-infrastructure)

