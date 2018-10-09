# Ansible Role: bpf-tools

Configure and install BPF tools (bcc, ply, bpftrace)

## Using the role
### Installation
```
ansible-galaxy install bpf-tools
```

### Example Playbook
```
  - hosts: all
    roles:
      - bpf-tools
```

### Variables

See [`defaults/main.yml`](defaults/main.yml).

## Testing the role

### Dependencies
- Bundler 1.13.0+
- Ruby 2.3.0+
- Docker 1.12.0+
- Vagrant
- Virtualbox
- See [`Gemfile`](Gemfile)
