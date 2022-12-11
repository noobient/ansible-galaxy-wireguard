# bviktor.wireguard

## Synopsys

This role serves as a skeleton for other Ansible Galaxy roles.

## Parameters

| Name | Required | Example | Description |
|---|---|---|---|
| `msg` | yes | `Hello world!` | Message to be displayed. |

## Examples

```yml
- include_role:
    name: bviktor.wireguard
  vars:
    msg: 'Hello world!'
```

## Return Values

N/A

## Support

| Platform | Support | Status |
|---|---|---|
| Linter | ✅ | [![Lint](https://github.com/noobient/ansible-wireguard/actions/workflows/lint.yml/badge.svg)](https://github.com/noobient/ansible-wireguard/actions/workflows/lint.yml) |
| AlmaLinux 8 | ✅ | [![AlmaLinux 8](https://github.com/noobient/ansible-wireguard/actions/workflows/almalinux-8.yml/badge.svg)](https://github.com/noobient/ansible-wireguard/actions/workflows/almalinux-8.yml) |
| AlmaLinux 9 | ✅ | [![AlmaLinux 9](https://github.com/noobient/ansible-wireguard/actions/workflows/almalinux-9.yml/badge.svg)](https://github.com/noobient/ansible-wireguard/actions/workflows/almalinux-9.yml) |
| Fedora 37 | ✅ | [![Fedora 37](https://github.com/noobient/ansible-wireguard/actions/workflows/fedora-37.yml/badge.svg)](https://github.com/noobient/ansible-wireguard/actions/workflows/fedora-37.yml) |
| Ubuntu 18.04 | ✅ | [![Ubuntu 18.04](https://github.com/noobient/ansible-wireguard/actions/workflows/ubuntu-18.04.yml/badge.svg)](https://github.com/noobient/ansible-wireguard/actions/workflows/ubuntu-18.04.yml) |
| Ubuntu 20.04 | ✅ | [![Ubuntu 20.04](https://github.com/noobient/ansible-wireguard/actions/workflows/ubuntu-20.04.yml/badge.svg)](https://github.com/noobient/ansible-wireguard/actions/workflows/ubuntu-20.04.yml) |
| Ubuntu 22.04 | ✅ | [![Ubuntu 22.04](https://github.com/noobient/ansible-wireguard/actions/workflows/ubuntu-22.04.yml/badge.svg)](https://github.com/noobient/ansible-wireguard/actions/workflows/ubuntu-22.04.yml) |
