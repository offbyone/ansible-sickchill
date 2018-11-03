Sickchill
=========
[![Build Status](https://travis-ci.org/wilfriedroset/sickchill.svg?branch=master)](https://travis-ci.org/wilfriedroset/sickchill)

Install [sickchill](https://github.com/sickchill/sickchill)

Requirements
------------

This role do not have requirements other than to be used on tested platforms.

Platforms
---------

This role has been tested on:

* Debian stretch (9)
* Ubuntu xenial (16.04)
* Ubuntu bionic (18.04)
* Centos 7

Role Variables
--------------

This role supports the following variables:
* sickchill_user: name of the user responsible for running sickchill daemon
* sickchill_group: name of the group of the user responsaible for running sickchill daemon
* sickchill_data: path where to store sickchill data
* sickchill_repo: git repository of sickchill
* sickchill_src: path where to store sickchill source
* sickchill_version: sickchill version to provision

Dependencies
------------

This role is standalone and do not depends on any other role.

Example Playbook
----------------

Use the role with all default variables:

```yaml
    - hosts: servers
      roles:
         - wilfriedroset.sickchill
```

Change the user:

```yaml
    - hosts: servers
      roles:
         - {role: 'wilfriedroset.sickchill', sickchill_user: 'pi', sickchill_group: 'pi'}
```

Install a specific version:

```yaml
    - hosts: servers
      roles:
         - {role: 'wilfriedroset.sickchill', sickchill_version: 'v2018.10.29-2'}
```

License
-------

GPLv3
