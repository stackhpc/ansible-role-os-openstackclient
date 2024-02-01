# NOTE:

This repository is no longer maintained - role has been moved to [Ansible
collection](https://docs.ansible.com/ansible/latest/collections_guide/index.html)
now ➡️ https://github.com/stackhpc/ansible-collection-openstack

OpenStack Client
================

This role can be used to install the python package ``python-openstackclient``.

Requirements
------------

Linux - none, macOS - brew.sh

Role Variables
--------------

`os_openstackclient_venv` is a path to a directory in which to create a
virtualenv.

`os_openstackclient_install_epel`: Whether to install EPEL repository package.

`os_openstackclient_install_package_dependencies`: Whether to install package
dependencies.

`os_openstackclient_version`: Version of python-openstackclient to install, or
latest if empty.

Dependencies
------------

None

Example Playbook
----------------

The following playbook installs openstackclient in a virtualenv.

    ---
    - name: Ensure openstackclient is installed
      hosts: localhost
      roles:
        - role: stackhpc.os-openstackclient
          os_openstackclient_venv: "~/os-openstackclient-venv"

Author Information
------------------

- Mark Goddard (<mark@stackhpc.com>)
