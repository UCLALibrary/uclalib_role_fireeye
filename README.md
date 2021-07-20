uclalib_role_fireeye
=========

Ansible role to install the FireEye Agent on RHEL systems

Requirements
------------

This role requires the following in your environment:
* RHEL 7+ OS
* uclalib custom yum repo installed - this is where the FireEye agent rpm resides

Role Variables
--------------

* `fireeye_agent_pkg` - defines the name of the fire eye agent package
* `fireeye_agent_install_path` - define the file system path where the fire eye agent is installed
* `fireeye_agent_exec` -  defines the file system path to the fire eye agent executable
* `fireeye_agent_config` - defines the file name of the fire eye agent configuration

Dependencies
------------

Required roles:
* `uclalib_role_uclalibrepo`

Example Playbook
----------------

```
---

- name: uclalib_fireeye.yml
  become: yes
  become_method: sudo
  hosts: all

  roles:
    - { role: uclalib_role_uclalibrepo }
    - { role: uclalib_role_fireeye }
```
