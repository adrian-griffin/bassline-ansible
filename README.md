# Ansible Role: Bassline

[![CircleCI](https://circleci.com/gh/bassline/ansible-role-bassline.svg?style=svg)](https://circleci.com/gh/bassline/ansible-role-bassline)
[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](LICENSE)

Ansible role for [Bassline KVM](https://github.com/bassline/bassline).

## Role Variables

Available variables are listed below, along with default values (see [defaults/main.yml](defaults/main.yml)):

```yaml
bassline_group: bassline
bassline_dir: /opt/bassline
bassline_repo: https://github.com/bassline/bassline.git
bassline_repo_branch: master
bassline_interface: '127.0.0.1'
bassline_port: 8000
bassline_keyboard_interface: /dev/hidg0
```

## Dependencies

* [bassline.ustreamer](https://github.com/bassline/ansible-role-ustreamer)
* [bassline.nginx](https://github.com/bassline/ansible-role-nginx)

## Example Playbook

#### `example.yml`

```yaml
- hosts: all
  roles:
    - role: ansible-role-bassline
```

### Running Example Playbook

```bash
ansible-galaxy install git+https://github.com/bassline/ansible-role-bassline.git
ansible-playbook example.yml
```

## License

MIT

## Author Information

This role was created in 2020 by [Adrian Griffin](http://adrian-griffin.io).
