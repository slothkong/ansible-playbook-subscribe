# Subscribe via Morpheus runtime

Dummy Ansible Playbook that runs from Morpheus runtime.

## Usage

1. Define the path to the playbook subdirectory:
```
export ANSIBLE_PLAYBOOK=subscribe_via_morpheus.yml
```

2. Download any dependencies:
```bash
ansible-galaxy role install -r requirements.yml -p ./roles
```

3. Create an `inventory.yml` file. For example:
```yaml
inventory:
  hosts:
    host:
      ansible_python_interpreter: /usr/bin/python3
      ansible_ssh_private_key_file: ~/.ssh/id_rsa
      ansible_host: 10.0.0.1
      ansible_user: root
```

4. Run the playbook:

```bash
ansible-playbook -i inventory.yml $ANSIBLE_PLAYBOOK
```