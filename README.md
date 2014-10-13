# Ansible Role: Java

[![Build Status](https://travis-ci.org/geerlingguy/ansible-role-java.svg?branch=master)](https://travis-ci.org/geerlingguy/ansible-role-java)

Installs Java for RedHat/CentOS 6.x and Debian/Ubuntu linux servers.

## Requirements

None.

## Forked from Daniel Groves excellent repo geerlingguy/ansible-role-java

Thanks Daniel

## Role Variables

Available variables are listed below, along with default values:

    java_packages:
      - java-1.6.0-openjdk

Set the version/development kit of Java to install, along with any other necessary Java packages. Some other options include are included in the distribution-specific files in this role's 'defaults' folder. Note that you **must** include this variable in order to have the proper version of Java installed, due to cross-platform compatibility issues (see: [Issue #8121](https://github.com/ansible/ansible/issues/8121)).

## Dependencies

None.

## Example Playbook

    - hosts: servers
      vars:
        java_packages:
          - java-1.6.0-openjdk
      roles:
        - { role: geerlingguy.java }

## License

MIT / BSD

## Author Information

This role was created in 2014 by [Jeff Geerling](http://jeffgeerling.com/), author of [Ansible for DevOps](http://ansiblefordevops.com/).
