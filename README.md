# NoMachine Install/Remove Role
***Version 1.0.0***
=========

A role that will install NoMachine. 

About: 
NoMachine is a fast and high quality remote desktop.

[NoMachine](https://www.nomachine.com/)

## Requirements
--------------

none

## Role Variables
--------------
The vars are deflaulted to the following below. You can override them within the playbook if needed.
```
vars:
    install: "true"
    install_path: /usr
    url_redhat: https://download.nomachine.com/download/6.4/Linux/
    url_debian: https://download.nomachine.com/download/6.4/Linux/
    url_suse: https://download.nomachine.com/download/6.4/Linux/
    version_redhat: nomachine_6.4.6_1_x86_64.rpm
    version_debian: nomachine_6.4.6_1_amd64.deb
    version_suse: nomachine_6.4.6_1_x86_64.tar.gz
```
## Dependencies
----------------

none

## Example Playbook
----------------
***You can enter the hostnames or groups on the CLI using***`--exrta-var "varaible_host=foo_servers"`
### With vars included.
```
---
- hosts: "{{ variable_host }}"
  become: yes
  become_user: root
  vars:
    - install: "true"
    - install_path: /usr
    - url_redhat: https://download.nomachine.com/download/6.4/Linux/
    - url_debian: https://download.nomachine.com/download/6.4/Linux/
    - url_suse: https://download.nomachine.com/download/6.4/Linux/
    - version_redhat: nomachine_6.4.6_1_x86_64.rpm
    - version_debian: nomachine_6.4.6_1_amd64.deb
    - version_suse: nomachine_6.4.6_1_x86_64.tar.gz
  roles: 
    - nomachine
```

### Without vars. 
```
---
- hosts: "{{ variable_host }}"
  become: yes
  become_user: root
  roles: 
    - nomachine
```
### With all host
```
---
- hosts: all
  become: yes
  become_user: root
  roles: 
    - nomachine
```
License
-------

FIU

Author Information
------------------

Joseph Martinez
