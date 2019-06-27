[![Build Status](https://travis-ci.org/lhazlewood/ansible-role-xcode-clt.svg?branch=master)](https://travis-ci.org/lhazlewood/ansible-role-xcode-clt)

# Ansible Role for Xcode Command Line Tools

Ansible role that installs Xcode Command Line Tools on Mac OS X >= 10.11 (El Capitan, Sierra, High Sierra, etc).

This role can be used in any playbook:

* regardless if Xcode is already installed or not
* regardless if the target host operating system is Mac or not.  It will only actually execute if the host OS is Mac, i.e. 
    
    `when: ansible_os_family == 'Darwin'`

There are no variables or configuration settings at all.

## Example Playbook

```yaml
- hosts: localhost
  roles:
    - lhazlewood.xcode_clt
```

## License

MIT / BSD
