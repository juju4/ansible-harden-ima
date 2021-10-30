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

## References

* https://sourceforge.net/p/linux-ima/wiki/Home/
* https://www.redhat.com/en/blog/how-use-linux-kernels-integrity-measurement-architecture
* https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html/managing_monitoring_and_updating_the_kernel/enhancing-security-with-the-kernel-integrity-subsystem_managing-monitoring-and-updating-the-kernel#enabling-integrity-measurement-architecture-and-extended-verification-module_enhancing-security-with-the-kernel-integrity-subsystem
* https://en.opensuse.org/SDB:Ima_evm#ima-grammar
* https://wiki.strongswan.org/projects/strongswan/wiki/IMA
* https://svs.informatik.uni-hamburg.de/publications/2020/2020-08-27-Bohling-IMA.pdf

## License

BSD 2-clause
