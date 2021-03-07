Ansible role : snmp_exporter
=========

Deploy and configure prometheus snmp_exporter

Requirements
------------

Ansible, ubuntu

Role Variables
--------------

Name | Default Value | Description
---|---|---
`snmp_exporter_version` |  "0.20.0" | current version
`snmp_exporter_install_dir` |  "/usr/local/bin" |
`snmp_exporter_repo_dir` |  "/var/tmp/archive" | 

```sh
mkdir -p /var/tmp/archive
cd /var/tmp/archive
wget https://github.com/prometheus/snmp_exporter/releases/download/v0.20.0/snmp_exporter-0.20.0.linux-amd64.tar.gz
```

Example Playbook
----------------

```yaml
---
- hosts: vmagent
  gather_facts: true
  connection: ssh
  roles:
    - v98765_exporter_snmp
```

License
-------

BSD
