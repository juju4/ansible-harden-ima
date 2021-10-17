[![Actions Status - Master](https://github.com/juju4/ansible-harden-ima/workflows/AnsibleCI/badge.svg)](https://github.com/juju4/ansible-harden-ima/actions?query=branch%3Amaster)
[![Actions Status - Devel](https://github.com/juju4/ansible-harden-ima/workflows/AnsibleCI/badge.svg?branch=devel)](https://github.com/juju4/ansible-harden-ima/actions?query=branch%3Adevel)

# harden-ima ansible role

Configure Linux kernel's Integrity Measurement Architecture (IMA)

## Requirements & Dependencies

### Ansible
It was tested on the following versions:
 * 4.3

### Operating systems

Tested on Ubuntu 18.04, 20.04, Centos 7 and 8.

## Example Playbook

Just include this role in your list.
For example

```
- host: myhost
  roles:
    - juju4.harden-ima
```

## Variables

N/A

## Continuous integration

```
$ pip install molecule docker
$ molecule test
$ MOLECULE_DISTRO=ubuntu:20.04 molecule test --destroy=never
```


## Troubleshooting & Known issues

* Some cloud providers may not support IMA in their stack or bug
Digital Ocean: get Kernel panic at reboot on Ubuntu 20.04 and 21.04. Centos8 image boots normally.

## License

BSD 2-clause
