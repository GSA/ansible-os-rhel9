# Redhat 9 GSA Benchmark

This role configures Red Hat Enterprise Linux (RHEL) 9.0 machine to be GSA compliant. Level 1 and 2 profiles will be applied by default based on [RHEL 9.0 GSA Benchmarks](https://docs.google.com/spreadsheets/d/1Bf0QBKHbEOLA8tHfqQy7REO90CMnOPVPpZZlE7Ijy8g/edit#gid=884169645)

## Role Variables

There are many role variables defined in ``./defaults/main.yml``.

**Hardening will be applied to the following configurations by default**:

- General Configurations
- Services Configurations
- Network Configurations
- Logging and Auditing Configurations
- Access, Authentication and Authorization Configurations
- System Maintenance Configurations

Above high level configurations and other fine-grained configurations can be enabled/disabled using variabled defined in in defaults/main.yml.

**The configuration will not**:

- Install and configure AIDE
- Install and configure NTP
- Configure the /etc/group wheel configurations

Other settings and services are listed. Please review to ensure they meet your organizational requirements.

## Dependencies

Ansible >= 2.7

## Example Playbook

```
---
- name: Harden Server
  hosts: all
  become: yes

  roles:
    - ansible-os-rhel9
```

## How to test locally

```
ansible-playbook playbook.yml --connection=local
```



## License

MIT.
