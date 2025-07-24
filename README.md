# Subscribe/Unsubscribe Ansible Playbooks

## Usage

1. Download any dependencies:
```bash
ansible-galaxy role install -r requirements.yml --roles-path ./roles
```

2. Create an `inventory.yml` file. For example:
```yaml
inventory:
    hosts:
        ansible_python_interpreter: /usr/bin/python3
        ansible_ssh_private_key_file: ~/.ssh/id_rsa
        ansible_host: 10.0.0.1
        ansible_user: root
```

3. Run the playbook:

```bash
ansible-playbook -i inventory.yml <playbook filename>
```
