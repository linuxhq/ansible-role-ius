# ansible-role-ius

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-ius.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-ius)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-ius-blue.svg?style=flat)](https://galaxy.ansible.com/linuxhq/ius)
[![License](https://img.shields.io/badge/license-GPLv3-brightgreen.svg?style=flat)](COPYING)

RHEL/CentOS - Inline with Upstream Stable

## Requirements

This role requires that you have the epel repository installed.

 * https://galaxy.ansible.com/linuxhq/epel/

## Role Variables

Available variables are listed below, along with default values:

    ius_disable_plugin: []
    ius_disablerepo: []
    ius_enable_plugin: []
    ius_enablerepo: []
    ius_packages: []
    ius_pkg: ius-release
    ius_rel: "{{ ansible_distribution_major_version }}"
    ius_repository_ius: false
    ius_repository_ius_gpgcheck: true
    ius_repository_ius_repo_gpgcheck: false
    ius_repository_ius_debuginfo: false
    ius_repository_ius_debuginfo_gpgcheck: true
    ius_repository_ius_debuginfo_repo_gpgcheck: false
    ius_repository_ius_source: false
    ius_repository_ius_source_gpgcheck: true
    ius_repository_ius_source_repo_gpgcheck: false
    ius_repository_ius_archive: false
    ius_repository_ius_archive_gpgcheck: true
    ius_repository_ius_archive_repo_gpgcheck: false
    ius_repository_ius_archive_debuginfo: false
    ius_repository_ius_archive_debuginfo_gpgcheck: true
    ius_repository_ius_archive_debuginfo_repo_gpgcheck: false
    ius_repository_ius_archive_source: false
    ius_repository_ius_archive_source_gpgcheck: true
    ius_repository_ius_archive_source_repo_gpgcheck: false
    ius_repository_ius_testing: false
    ius_repository_ius_testing_gpgcheck: true
    ius_repository_ius_testing_repo_gpgcheck: false
    ius_repository_ius_testing_debuginfo: false
    ius_repository_ius_testing_debuginfo_gpgcheck: true
    ius_repository_ius_testing_debuginfo_repo_gpgcheck: false
    ius_repository_ius_testing_source: false
    ius_repository_ius_testing_source_gpgcheck: true
    ius_repository_ius_testing_source_repo_gpgcheck: false
    ius_rpm_key: "{{ '/etc/pki/rpm-gpg/RPM-GPG-KEY-IUS-' + ius_rel }}"

All repositories are disabled by default.

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.ius
          ius_repository_ius: true

## License

Copyright (C) 2018 Taylor Kimball <tkimball@linuxhq.org>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.
