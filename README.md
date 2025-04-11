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
### horizon-cli Local Scan

To lunch a local scan, run the role with the `local_campaign` variable set to your discovery campaign's name in Horizon.

```yaml
- hosts: all
  roles:
    - role: 'evertrust.horizon_cli'
      vars:
        local_campaign: '<localscan_campaign_name>'
```


### horizon-cli Network Scan

To lunch a local scan, run the role with the `net_campaign` variable set to your discovery campaign's name in Horizon.

```yaml
- hosts: all
  roles:
    - role: 'evertrust.horizon_cli'
      vars:
        net_campaign: '<networkscan_campaign_name>'
```