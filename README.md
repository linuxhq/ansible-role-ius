# ansible-role-ius

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-ius.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-ius)

RHEL/CentOS - Inline with Upstream Stable

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    ius_pkg: ius-release
    ius_rel: "{{ ansible_distribution_major_version }}"
    ius_repos:
      ius: False
      ius_debuginfo: False
      ius_source: False
      ius_archive: False
      ius_archive_debuginfo: False
      ius_archive_source: False
      ius_dev: False
      ius_dev_debuginfo: False
      ius_dev_source: False
      ius_testing: False
      ius_testing_debuginfo: False
      ius_testing_source: False

All repositories are disabled by default.

## Dependencies

 * https://galaxy.ansible.com/linuxhq/epel/

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.ius
          ius_repos:
            ius: True

## License

GPLv3

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org).
