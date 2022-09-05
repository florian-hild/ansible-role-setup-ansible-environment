Ansible Role: setup-ansible-environment
=========

- Create anisble user
- Add public key to authorized_key file
- Deploy supcis_sudoers configuration

Installation
------------

```shell
$ ansible-galaxy install setup-ansible-environment
```

To be able to update later and eventually to modify it, prefer using `requirements.yml` with the git source:

```yaml
- name: setup-ansible-environment
  src: git@github.com:florian-hild/ansible-role-setup-ansible-environment.git
  scm: git
  version: main
```
And then download it with `ansible-galaxy`:

```shell
$ ansible-galaxy install -r requirements.yml
```

Using `git`, you'll have to be carefull to folder name:

```shell
$ git clone git@github.com:florian-hild/ansible-role-setup-ansible-environment.git setup-ansible-environment
```

Role Variables
--------------

Available variables are listed below, along with their default values (see `defaults/main.yml`):

Default:
 ```yaml
remote_ansible_username: 'ansible'
 ```

Example:
 ```yaml
remote_ansible_username: 'ansible'
remote_ansible_uid: 2999
remote_ansible_password: '$6$pwwdpnEwKcuassHX$B1PiUVngyOj2py4TGJDVu7lQSNiJYwwp1wQNBbYCHLu8tozpSB71AfqJmtvMzz9Eywb7x4ZFqf4jHyhEXBtGE0'
 ```

Ansible facts:
  - ansible_date_time.date