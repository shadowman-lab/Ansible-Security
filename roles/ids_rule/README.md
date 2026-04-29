<!-- This was created with Claude Code -->

ids_rule
========

An Ansible role for ids rule.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **ids_provider_list**: defaults file for ids_rule
  - Default: `['snort']`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: ids_rule
      vars:
        ids_provider_list: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
