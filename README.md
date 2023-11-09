# ansible-role-horizon-cli

This Ansible role automates the deployment and the configuration of the Horizon client on a RHEL machine.

## Requirements

Ansible 2.9 or higher.

## Usage

### horizon-cli installation

To use this role, assign it to an host and pass the variables you wish to preconfigure:
```yaml
---
- hosts: all
  roles:
    - role: 'evertrust.horizon_cli'
      vars:
        endpoint: 'https://horizon.company.com'
```

Variables that can be passed to this role are document in the [defaults/main.yml](defaults/main.yml) file.

### horizon-cli uninstallation

To uninstall the Horizon client, run the role with the `run_option` variable set to `uninstall`:
```yaml
- hosts: all
  roles:
    - role: 'evertrust.horizon_cli'
      vars:
        run_option: 'uninstall'
```

