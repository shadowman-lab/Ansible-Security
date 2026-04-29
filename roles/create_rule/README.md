<!-- This was created with Claude Code -->

create_rule
===========

An Ansible role for create rule.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **rule_name**: Variable used in: {{ palo_username }}
  - Default: `Attacker to Snort Rule`

* **description**: Variable used in: {{ rule_name }}
  - Default: `An Ansible attacker rule`

* **source_zone**: Variable used in: {{ rule_name }}
  - Default: `['any']`

* **destination_zone**: Variable used in: {{ rule_name }}
  - Default: `['any']`

* **source_ip**: IP address
  - Default: `{{ hostvars[source_vm | default('attack.shadowman.dev')]['ip_addr'] }}`

* **source_user**: Username or user account name
  - Default: `['any']`

* **destination_ip**: IP address
  - Default: `{{ hostvars[destination_vm | default('ids.shadowman.dev')]['ip_addr'] }}`

* **category**: Configuration parameter for service task
  - Default: `['any']`

* **application**: Configuration parameter for service task
  - Default: `['any']`

* **service**: Configuration parameter for service task
  - Default: `['any']`

* **hip_profiles**: Configuration parameter for service task
  - Default: `['any']`

* **actiontaken**: Configuration parameter for service task
  - Default: `allow`

* **state**: Configuration parameter for service task
  - Default: `present`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: create_rule
      vars:
        rule_name: <value>
        description: <value>
        source_zone: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
