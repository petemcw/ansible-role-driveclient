# Rackspace `driveclient` Role for Ansible

This role installs the `driveclient` agent which works with Rackspace Cloud Backup.

## Requirements

This role requires [Ansible](http://www.ansibleworks.com/) version 1.4 or higher and the Debian/Ubuntu platform.

## Role Variables

The variables that can be passed to this role and a brief description about
them are as follows (additional variables are available in the source):

```yaml
# The API credentials for Rackspace driveclient
driveclient_enabled: false
driveclient_username: ""
driveclient_apikey: ""
```

## Examples

1. Install driveclient with the defaults

    ```yaml
    ---
    # This playbook installs driveclient

    - name: Apply driveclient to all nodes
      hosts: all
      roles:
        - driveclient
    ```

2. Install driveclient with custom credentials

    ```yaml
    ---
    # This playbook installs driveclient

    - name: Apply driveclient to all Rackspace nodes
      hosts: rackspace
      roles:
        - { role: driveclient,
            driveclient_enabled: true,
            driveclient_username: "augustash",
            driveclient_apikey: "asdfasdfasdfasdf"
          }
    ```

## Dependencies

None.

## License

MIT.
