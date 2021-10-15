chrony
=========

Basic playbook as an exercise in:

* simple variables
* handlers
* commenting lines in files (replacing)
* conditions

This playbook will:

* install [chrony](https://chrony.tuxfamily.org/) on one or more GNU/Linux hosts
* erase (uncomment) the current ntp servers or pools unless no `ntp_server` variable is found
* use an ntp server, defined by you by setting the `ntp_server` variable

Variables
--------------

* `ntp_server`: Contains the chosen upstream NTP server. Set this variable as a host\_var or group\_var.

Set this to your ISP's NTP server. (Probably **ntp.telenet.be** or **ntp.skynet.be**)

Example of setting the variable in an ini-style inventory:

```ini
[mygroup:vars]
ntp_server: ntp.howest.be
```

Example of setting the variable in a host\_vars or group\_vars file:

```YAML
---
ntp_server: ntp.howest.be
```

Usage
--------------

Log in on the nodes as **root**, or make use of the [become](https://docs.ansible.com/ansible/latest/user_guide/become.html) plugin.