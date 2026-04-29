<!-- This was created with Claude Code -->

delete_rule
===========

An Ansible role for delete rule.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **rule_name**: Variable used in: {{ palo_username }}
  - Default: `Ansible Attacker Rule`

* **state**: Variable used in: {{ rule_name }}
  - Default: `absent`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: delete_rule
      vars:
        rule_name: <value>
        state: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
