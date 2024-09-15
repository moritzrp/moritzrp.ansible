# Ansible Role: podman

Install Podman.

## Requirements

None.

## Role Variables

```yaml
podman_login_lingering_users: []
```

## Dependencies

None.

## Example Playbook

```yaml
---
- name: Install Podman
  hosts: all
  gather_facts: false
  become: true
  tasks:
    - name: Install Podman
      ansible.builtin.include_role:
        name: moritzrp.ansible.podman
      vars:
        podman_login_lingering_users:
          - myuser
```

## License

MIT

## Author Information

moritzrp
