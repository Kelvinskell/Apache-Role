Role Name
=========

A brief description of the role goes here.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

This role makes use of two variables:
- doc_root
- domain

The _doc_root_ variable represents the document root and is declared in the `main.yml` file of the `vars` directory.
This variable is more permanent and is not expected to be trivially changed by the user.

The _domain_ variable is a more temporary variable hence it is declared in the `defaults` directory.

This variable represents the domain name of the website to be provisioned alongside the server and is expected to change frequently - as per requirements.


Example Playbook
----------------
- name: Provision Apache Web Server
  hosts: localhost
  become: true
  roles:
  - Apache-Role


