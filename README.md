Ansible Role: clamav
====================

[ClamAV](https://www.clamav.net/) is an open source antivirus engine for detecting trojans, viruses, malware & other malicious threats.

This role is part of the [Mailserver](https://github.com/mailserver) project.

Examples
--------

### ClamAV via Socket

```yaml
- role: mailserver.clamav
  milter:
    socket_path: "/var/spool/postfix/milters/clamav-milter.ctl"
    group: "milter"
```

The directory `/var/spool/postfix/milters` is expected to exist with read/write access to the milter_socket_group.
