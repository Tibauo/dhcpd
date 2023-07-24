# DHCP

Install & configure DHCP

## Requirements

```
```

## Var

```
pxe:
  - dhcp_subnet: 172.16.1.0
    dhcp_gw: 172.16.1.1
    dhcp_broadcast: 172.16.1.255
    dhcp_mask: 255.255.255.0
    dhcp_addr: 172.16.1.10
    first: 172.16.1.20
    last: 172.16.1.100
    servers:
    - hostname: satellite.monlab.local
      mac_address: 52:54:00:67:15:df
      ip_pxe: 172.16.1.20
      ip_mgmt: 172.17.1.20
      ip_proxy: 172.18.1.20
      release: 8.6
```

## Playbook

```
- name: pxe
  hosts: pxe
  gather_facts: no
  roles:
    - dhcpd
```
