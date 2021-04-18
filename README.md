 ansible_role_mailserver_preperations
======================================
Preperation, User and Database Configuration ansible role for a mailserver Setup

```
ATTENTION

THIS IS A WORK IN PROGRESS

BE CAREFULL, IF YOU THINK ABOUT USING IT. EVERYTHING HERE CAN CHANGE!!!

IT IS NOT FULLY DOCUMENTATED, NOT EVEN THE OTHER REQUIRED ROLES
```

 What is the purpose of this Ansible role?
-------------------------------------------

The Ansible role was created when [L3D](https://github.com/DO1JLR) set up a mail server. This role performs a few preliminary tasks for the mail server setup.

The role is intended to be used in conjunction with the following Ansible roles to set up a mail server. The setup was largely inspired by the instructions on [https://thomas-leister.de/mailserver-debian-buster/](thomas-leister.de/mailserver-debian-buster/).

 What exactly is being done?
-----------------------------

As an optional step, a simple version check can be performed.

First, the hostname of the system is set. For a mailing server, the name of the server used is an important part. For more details have a look at [tasks/hosts.yml](tasks/hosts.yml)

Next, create a user and a group for the mail history. And a few folders that are needed. More details in [tasks/user.yml](tasks/user.yml).

And as the last important step, a template for creating a database is deployed. And the data for the MySQL database is deployed. This requires that a mysql database exists before.

 Testing
----------
We are using some github actions for publishing and linting checks. If you know a good testing method for ansible that is using systemd stuff please let us know. For more infos about the tests, please have a look at the github marketplace.

| test status | Github Marketplace |
| :---------  | :----------------  |
| [![Ansible Lint check](https://github.com/DO1JLR/ansible_role_mailserver_preperations/workflows/Ansible%20Lint%20check/badge.svg)](https://github.com/DO1JLR/ansible_role_mailserver_preperations/actions?query=workflow%3A%22Ansible+Lint+check%22) | [ansible-lint action](https://github.com/marketplace/actions/ansible-lint)
