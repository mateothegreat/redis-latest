# redis-latest ansible role

This role will install the latest version of redis using the remi repo
for centos 7.

## Variables

```yaml
redis:
  bind: "0.0.0.0"
  port: "6379"
```

## Example Usage

Add the following to a file like `playbook.yaml`:

```yaml
- hosts: monitoring
  roles:
    - role: "mateothegreat.redis_latest"
      vars:
        redis:
          bind: "0.0.0.0"
          port: "6379"
```

Run with `ansible-playbook -i <your inventory file> playbook.yaml`.
