# ansible-consul role
Installs and configures Hashicorp Consul for Ubuntu trusty/xenial servers.

## Requirements
![Ansible](https://img.shields.io/badge/ansible-2.8.2-green)

## Dependencies
No dependencies.


## Role variables
| Parameter    | Default |
|--------------|----------|
| `consul_version` | `1.0.0` |
| `consul_os` | `linux` |
| `consul_arch` | `amd64` |
| `consul_url` | `https://releases.hashicorp.com/consul/{{ consul_version }}/consul_{{ consul_version }}_{{ consul_os }}_{{ consul_arch }}.zip` |
| `consul_configdir` | `/etc/consul` |
| `consul_configdir_ssl` | `{{ consul_configdir }}/ssl` |
| `consul_user` | `consul` |
| `consul_group` | `bin` |
| `consul_manage_group` | `true` |
| `consul_service_state` | `started` |
| `consul_service_enabled` | `yes` |
| `consul_service_execstartpre` | `[]` |
| `consul_secrets` | `{}` |
| `consul_node_name` | `{{ ansible_fqdn }}` |
| `consul_client_addr` | `127.0.0.1` |
| `consul_acl_default_policy` | `deny` |
| `consul_acl_down_policy` | `deny` |
| `consul_acl_ttl` | `30s` |
| `consul_addresses` | `dns: 127.0.0.1 http: 127.0.0.1 https: 127.0.0.1` |
| `consul_bind_addr` | `127.0.0.1` |
| `consul_bootstrap` | `false` |
| `consul_bootstrap_expect` | `0` |
| `consul_advertise_addr` | `{{ ansible_default_ipv4.address }}` |
| `consul_datacenter` | `dc1` |
| `consul_data_dir` | `/var/consul` |
| `consul_log_level` | `INFO` |
| `consul_ports` | `dns: 8600 http: 8500 https: 8501 serf_lan: 8301 serf_wan: 8302 server: 8300` |
| `consul_retry_interval` | `30s` |
| `consul_retry_join` | `[]` |
| `consul_retry_max` | `0` |
| `consul_server` | `false` |
| `consul_ui` | `false` |
| `consul_tls_enable` | `false` |
| `consul_tls_verify_incoming` | `false` |
| `consul_tls_verify_incoming_rpc` | `true` |
| `consul_tls_verify_outgoing` | `true` |
| `consul_tls_verify_server_hostname` | `false` |
| `consul_performance` | `raft_multiplier: 5` |
| `consul_services` | `{}` |
| `consul_extra_services` | `{}` |
