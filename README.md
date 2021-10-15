# NTP with chrony

## Variables

* `ntp_server`: Contains the chosen NTP server. Set this variable as a host\_var or group\_var.

## Example

Setting the variable in an inventory:

```ini
[howest_proxmox:vars]
ntp_server: ntp.howest.be
```

or in a group\_vars file (howest\_proxmox.yaml):

```YAML
---
ntp_server: ntp.howest.be
```
