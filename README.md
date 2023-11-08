# noobient.wireguard

## Synopsys

This role allows you to install and configure a WireGuard server.

## Parameters

| Name | Required | Example | Description |
|---|---|---|---|
| `wg_endpoint` | no | `vpn.foo.com` | The FQDN / IP address of your WireGuard server. Clients will connect to this address. Defaults to your server's primary IP address. |
| `wg_ip` | no | `192.168.0.1` | The "virtual" IP address of the WireGuard Server on the tunnel network. Clients will be assigned adjacent IPs automatically.  Defaults to `10.10.10.1`. |
| `wg_port` | no | `12345` | The WireGuard server port. Defaults to `44444`. |
| `wg_clients` | no | `10` | The number of allowed clients. Defaults to `5`. |
| `wg_dns` | no | `9.9.9.9` | The DNS server clients will use for name resolution. Defaults to `1.1.1.1` (Cloudflare). |
| `wg_tunnel` | no | `full` | Tunnel type, can be either `full` (all client traffic goes through the server) or `split` (only tunnel traffic goes through). Defaults to `split`. |
| `wg_users` | no | `me,myself,irene` | Comma separated list of nick names for your users. Must be the same number as `wg_clients`. No default values. |
| `wg_repo` | no | `https://github.com/smitty/wg-config ` | HTTP URL of the GitHub repo where you want to push your generated WireGuard config files. No default values. |
| `wg_credential` | no | `https://smitty%40gmail.com:TOKEN_STUFF@github.com` | Your GitHub [personal access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) for the repo specified in `wg_repo`. No default values. |

## Examples

```yml
- include_role:
    name: noobient.wireguard
  vars:
    wg_endpoint: 'vpn.killingfloor2.party'
    wg_clients: '6'
    wg_tunnel: 'split'
```

## Return Values

N/A

## Support

| Platform | Support | Status |
|---|---|---|
| Linter | ✅ | [![Lint](https://github.com/noobient/ansible-galaxy-wireguard/actions/workflows/lint.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-wireguard/actions/workflows/lint.yml) |
| AlmaLinux 8 | ✅ | [![AlmaLinux 8](https://github.com/noobient/ansible-galaxy-wireguard/actions/workflows/almalinux-8.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-wireguard/actions/workflows/almalinux-8.yml) |
| AlmaLinux 9 | ✅ | [![AlmaLinux 9](https://github.com/noobient/ansible-galaxy-wireguard/actions/workflows/almalinux-9.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-wireguard/actions/workflows/almalinux-9.yml) |
| Fedora 37 | ✅ | [![Fedora 37](https://github.com/noobient/ansible-galaxy-wireguard/actions/workflows/fedora-37.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-wireguard/actions/workflows/fedora-37.yml) |
| Ubuntu 18.04 | ✅ | [![Ubuntu 18.04](https://github.com/noobient/ansible-galaxy-wireguard/actions/workflows/ubuntu-18.04.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-wireguard/actions/workflows/ubuntu-18.04.yml) |
| Ubuntu 20.04 | ✅ | [![Ubuntu 20.04](https://github.com/noobient/ansible-galaxy-wireguard/actions/workflows/ubuntu-20.04.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-wireguard/actions/workflows/ubuntu-20.04.yml) |
| Ubuntu 22.04 | ✅ | [![Ubuntu 22.04](https://github.com/noobient/ansible-galaxy-wireguard/actions/workflows/ubuntu-22.04.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-wireguard/actions/workflows/ubuntu-22.04.yml) |
