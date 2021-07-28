# Ansible-Role: OpenVPN Clinet

This role can be used to install and configure [OpenVPN](https://openvpn.net/) clients.

## Role Variables

ToDo

## Example Playbook

```yaml
- hosts: clients
  roles:
    - openvpn-client 
  vars:
    openvpn_client_ca: "{{ lookup('file', 'openvpn/ca.crt') }}"
    openvpn_client_configs:
      - name: work
        remote: "192.42.13.37"
        instances:
          - port: 1194
            proto: udp
        cert: "{{ lookup('file', 'openvpn/client.crt') }}"
        key: "{{ lookup('file', 'openvpn/client.key') }}"
```

## License

GPL-3.0