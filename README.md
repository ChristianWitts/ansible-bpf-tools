# Ansible Role: bpf-tools

Configure and install BPF tools (bcc, ply, bpftrace)

## Using the role

### Installation

```shell
ansible-galaxy install bpf-tools
```

### Example Playbook

```yaml
  - hosts: all
    roles:
      - bpf-tools
```

### Variables

See [`defaults/main.yml`](defaults/main.yml).

## Testing the role

### Dependencies

- Ansible 2.2+
- Molecule
- Docker 1.12.0+

## License

MIT
