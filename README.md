win_profile_redir
=========
[![Build Status](https://travis-ci.org/pyrotimux/pyrotimux.ProfileRedir.png?branch=master)](https://travis-ci.org/pyrotimux/pyrotimux.ProfileRedir)
Windows Profile Redirection.

Requirements
------------

WMF 5 (or powershell) on window box.

Role Variables
--------------
Please pass in the variable below. Example is shown below.
```
# users to change the registry.
  users:
    - { name: 'ichiban', pass: 'ichiV@gran7' }
    - { name: 'niban', pass: 'niV@gran7' }
    - { name: 'sanban', pass: 'sanV@gran7'}
    - { name: 'yonban', pass: 'yonV@gran7'}

# name of the file server and path. 
# If my file server is KGSTRGUTL and drive is c$ and path is profiles then
  file_server: KGSTRGUTL\\c$\\profiles
```

Dependencies
------------

You need the library folder in your ansible directory. It has the dsc modules needed for the play to work.

Also recommend setuping the folder with the win_profile_setup role first. They also share the vars.

https://github.com/pyrotimux/win_profile_setup

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
```
- hosts: all
  gather_facts: true
  roles:
     - win_profile_redir
```

License
-------

MIT

Author Information
------------------

chaosmuskey@gmail.com
