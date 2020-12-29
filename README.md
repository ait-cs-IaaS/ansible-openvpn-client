OpenVPN Clinet
=========

This role can be used to install and configure OpenVPN clients.


Role Variables
--------------

ToDo

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
```yaml
    - hosts: clients
      roles:
         - role: openvpn-client 
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

License
-------

MIT