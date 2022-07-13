Role Name
=========

Apache-Role is an ansible role that automates the provisioning of Apache Web Servers on both Debian and RedHat Linux hosts.

Requirements
------------

You only need to have ansible installed on the controlling machine.

With just python and ssh installed on your fleet of servers, you're free to go!

**N.B:** This role was developed for only Debian and RedHat Linux based distributions.

All of the tasks will certainly be skipped if the above confition is not met. But with a little tweaking, you can make the role serve your purposes on a non-conforming Linux distro.

Role Variables
--------------

This role makes use of two variables:

__- doc_root__

__- domain__

The _doc_root_ variable represents the document root and is declared in the `main.yml` file of the `vars` directory.
This variable is more permanent and is not expected to be trivially changed by the user.

The _domain_ variable is a more temporary variable hence it is declared in the `defaults` directory.

This variable represents the domain name of the website to be provisioned alongside the server and is expected to change frequently - as per requirements.


Example Playbook
----------------
\-  name: Provision Apache Web Server

    hosts: localhost
   
    become: true
   
    roles:
   
      - Apache-Role


