Ansible Role: clamav
====================

[ClamAV](https://www.clamav.net/) is an open source antivirus engine for detecting trojans, viruses, malware & other malicious threats.

This role is part of the [Mailserver](https://github.com/mailserver) project.

Examples
--------

### ClamAV via Socket

```yaml
- role: clamav
  milter_socket_path: "/var/spool/postfix/milters/clamav-milter.ctl"
  milter_socket_group: "milter"
  additional_group_memberships: [ "milter" ]
```

The directory `/var/spool/postfix/milters` is expected to exist with read/write access to the milter_socket_group.
