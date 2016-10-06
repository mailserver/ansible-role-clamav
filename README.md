Ansible Role: clamav
====================

[ClamAV](https://www.clamav.net/) is an open source antivirus engine for detecting trojans, viruses, malware & other malicious threats.

This role is part of the [Mailserver](https://github.com/mailserver) project.

Configuration
-------------

### clamav_user

Default: `clamav`

The ClamAV user will be created on the target and run the clamd and clamav-milter daemons.

### clamav_milter_group

Default: `milter`

The milter group will be created as system group on the target. The milter daemon will allow the milter group to access the milter socket.

### clamav_config

This variable is a structured dict that allows to pass individual configuration options to Freshclam, ClamAV and ClamAV-Milter daemons. The defaults from `clamav_default_config` can be overridden using this configuration variable.


Examples
--------

### ClamAV via Socket

```yaml
- role: mailserver.clamav
  clamav_config:
    freshclam:
      Check: 12 # update every 12 hours
```
