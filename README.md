# ansible-role-ipxe

![GitHub](https://img.shields.io/github/license/jomrr/ansible-role-ipxe) ![GitHub last commit](https://img.shields.io/github/last-commit/jomrr/ansible-role-ipxe) ![GitHub issues](https://img.shields.io/github/issues-raw/jomrr/ansible-role-ipxe) ![Travis (.com) branch](https://img.shields.io/travis/com/jomrr/ansible-role-ipxe/main?label=travis) [![Molecule](https://github.com/jomrr/ansible-role-ipxe/actions/workflows/molecule.yml/badge.svg)](https://github.com/jomrr/ansible-role-ipxe/actions/workflows/molecule.yml)

**Ansible role for installing iPXE and setting up TFTP Root.**

## Supported Platforms

| OS Family | Distribution  | Latest | Supported Version(s) | Comment |
|-----------|---------------|--------|----------------------|---------|
| Alpine    | Alpine        | :heavy_check_mark: | 3.12, 3.13 | |
| Archlinux | Archlinux     | :heavy_check_mark: | - | |
|           | Manjaro       | :heavy_check_mark: | - | |
| Debian    | Debian        | :heavy_check_mark: | 10, 11 | |
|           | Ubuntu        | :heavy_check_mark: | 18.04, 20.04 | |
| RedHat    | Almalinux     | :heavy_check_mark: | 8 | |
|           | Amazonlinux   | :x: | - | not tested, image not working |
|           | Centos        | :heavy_check_mark: | 8 | |
|           | Fedora        | :heavy_check_mark: | 33, 34, Rawhide | |
|           | Oraclelinux   | :heavy_check_mark: | 8 | |
| Suse      | OpenSuse Leap | :heavy_check_mark: | 15.1, 15.2, 15.3 | |
|           | Tumbleweed    | :heavy_check_mark: | - | |

## Requirements

Ansible 2.9 or higher.

## Variables

Variables and defaults for this role.

### defaults/main.yml

```yaml
ipxe_role_enabled: false
```

## Dependencies

None.

## Example Playbook

```yaml
---
# role: ansible-role-ipxe
# play: ipxe
# file: ipxe.yml

- hosts: all
  become: true
  gather_facts: true
  vars:
    ipxe_role_enabled: true
  roles:
    - role: ansible-role-ipxe
```

## License and Author

- Author:: [jomrr](https://github.com/jomrr/)
- Copyright:: 2021, [jomrr](https://github.com/jomrr/)

Licensed under [MIT License](https://opensource.org/licenses/MIT).
See [LICENSE](https://github.com/jomrr/ansible-role-ipxe/blob/master/LICENSE) file in repository.

## References

- [ArchWiki](https://wiki.archlinux.org/)
