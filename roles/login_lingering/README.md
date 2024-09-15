# Ansible Role: login_lingering

Enable login lingering for a user.

## Requirements

None.

## Role Variables

### Defaults

```yaml
login_lingering_systemd_path: /var/lib/systemd/linger
```

### Parameters

```yaml
login_lingering_user: ""
```

## Dependencies

None.

## Example Playbook

```yaml
---
- name: Enable lingering for user
  hosts: all
  gather_facts: false
  become: true
  tasks:
    - name: Enable lingering
      ansible.builtin.include_role:
        name: moritzrp.ansible.login_lingering
      vars:
        podman_login_lingering_users:
          - myuser
```

## License

MIT

## Author Information

- moritzrp
