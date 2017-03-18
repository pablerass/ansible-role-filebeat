# Filebeat

Basic _filebeat_ role. It works for _Windows_ and _Ubuntu_ platforms.

Defines a standard prospector called _dummy_ because is necessary to avoid run
errors in role service configuration.

Any other prospector can be added to `filebeat_conf_dir` folder.

## Role Variables

`filebeat_logstash_hosts`.

## Example Playbook

- hosts: servers
  become: yes
  roles:
    - { role: filebeat, filebeat_logstash_hosts: ["192.168.0.1", "192.168.0.2"] }
