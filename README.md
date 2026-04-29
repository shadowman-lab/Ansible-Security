<!-- This was created with Claude Code -->

# Security Automation

[![Contribute](https://img.shields.io/badge/OpenShift-Dev%20Spaces-525C86?logo=redhatopenshift&labelColor=EE0000)](https://devspaces.apps.ocp.shadowman.dev/#https://github.com/shadowman-lab/Ansible-Security)


This directory contains Ansible automation for security management and operations.

## Overview

The Security automation provides playbooks and roles for managing and configuring
security infrastructure and services.

## Roles

| Role | Description |
| ---- | ----------- |
| [create_rule](roles/create_rule/README.md) | Role for create rule |
| [delete_rule](roles/delete_rule/README.md) | Role for delete rule |
| [disable_log_forwarding_palo](roles/disable_log_forwarding_palo/README.md) | Role for disable log forwarding palo |
| [disable_log_forwarding_snort](roles/disable_log_forwarding_snort/README.md) | Role for disable log forwarding snort |
| [enable_log_forwarding_palo](roles/enable_log_forwarding_palo/README.md) | Role for enable log forwarding palo |
| [enable_log_forwarding_snort](roles/enable_log_forwarding_snort/README.md) | Role for enable log forwarding snort |
| [ids_config](roles/ids_config/README.md) | Role for ids config |
| [ids_rule](roles/ids_rule/README.md) | Role for ids rule |
| [ids_rule_facts](roles/ids_rule_facts/README.md) | Role for ids rule facts |
| [remove_log_forwarding_palo](roles/remove_log_forwarding_palo/README.md) | Role for remove log forwarding palo |
| [security_hostroutes](roles/security_hostroutes/README.md) | Role for security hostroutes |
| [set_log_forwarding_palo](roles/set_log_forwarding_palo/README.md) | Role for set log forwarding palo |
| [shadowman_cert_check](roles/shadowman_cert_check/README.md) | Role for shadowman cert check |
| [update_panorama](roles/update_panorama/README.md) | Role for update panorama |
| [web_attack_start](roles/web_attack_start/README.md) | Role for web attack start |
| [web_attack_stop](roles/web_attack_stop/README.md) | Role for web attack stop |

## Playbooks

| Playbook | Description | Target Hosts |
| -------- | ----------- | ------------ |
| add_allow_rule.yml | Playbook for add allow rule | localhost |
| add_block_rule.yml | Playbook for add block rule | localhost |
| certificatereport.yml | Playbook for certificatereport | all |
| remove_log_forwarding_palo.yml | Playbook for remove log forwarding palo | localhost, qradar.shadowman.dev |
| remove_log_forwarding_snort.yml | Playbook for remove log forwarding snort | snort.shadowman.dev, qradar.shadowman.dev |
| remove_palo_rule.yml | Playbook for remove palo rule | localhost |
| setup networking.yml | Playbook for setup networking | all |
| setup_log_forwarding_palo.yml | Playbook for setup log forwarding palo | localhost, qradar.shadowman.dev |
| setup_log_forwarding_snort.yml | Playbook for setup log forwarding snort | snort.shadowman.dev, qradar.shadowman.dev |
| snort_rule_add.yml | Playbook for snort rule add | snort.shadowman.dev |
| snort_rule_remove.yml | Playbook for snort rule remove | snort.shadowman.dev |
| snort_rule_verify.yml | Playbook for snort rule verify | snort.shadowman.dev |
| update_panorama.yml | Playbook for update panorama | localhost |
| web_attack_simulation_start.yml | Playbook for web attack simulation start | attacker.shadowman.dev |
| web_attack_simulation_stop.yml | Playbook for web attack simulation stop | attacker.shadowman.dev |

## Usage

### Running with ansible-navigator

```bash
# Run a playbook
ansible-navigator run add_allow_rule.yml

# Run in stdout mode
ansible-navigator run add_allow_rule.yml -m stdout
```

### Using roles

```yaml
- hosts: target_hosts
  roles:
    - create_rule
```

## Requirements

- Ansible 2.9 or higher (via ansible-navigator)
- Required collections (see `collections/requirements.yml` if present)
- Appropriate access credentials configured via environment variables

## Directory Structure

```
Ansible-Security/
├── roles/              # Ansible roles
├── *.yml               # Playbooks
├── collections/        # Collection dependencies (if present)
└── ansible-navigator.yml  # Navigator configuration
```
